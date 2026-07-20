# Asana: Get a team

Retrieves a team from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-team?connectionId=$CONNECTION_ID&teamGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-team?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamGid` | string | yes | Asana team gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "name": "Ava Chen",
      "organization": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "permalinkUrl": "https://example.com",
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `name` | string |  |
| `organization.gid` | string |  |
| `organization.name` | string |  |
| `organization.resourceType` | string |  |
| `permalinkUrl` | string |  |
| `resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET teams/:team_gid` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-team.md) for the provider-specific parameters and requirements.

