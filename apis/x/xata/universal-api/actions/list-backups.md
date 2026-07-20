# Xata: List project backups



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-backups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-backups?connectionId=$CONNECTION_ID&organizationID=string&projectID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "projectID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-backups?${params}`, {
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
| `organizationID` | string | yes | Unique identifier of the organization containing the project |
| `projectID` | string | yes | Unique identifier of the project to retrieve backups for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backups": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backups` | array<object> | list of backups within the project |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/projects/:projectID/backups` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-backups.md) for the provider-specific parameters and requirements.

