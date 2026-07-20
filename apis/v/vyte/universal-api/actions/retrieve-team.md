# Vyte: Retrieve Team

Retrieves a team from Vyte.

```
GET https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-team?${params}`, {
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
| `teamId` | string | no | The Vyte team ID. Default: `69caa901349c1a3356a285de`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "extid": "string",
      "name": "Ava Chen",
      "organization": "string",
      "public": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `extid` | string |  |
| `name` | string |  |
| `organization` | string |  |
| `public` | boolean |  |

## Native endpoint

Through the native Vyte API, this operation is `GET v2/teams/:team_id` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-team.md) for the provider-specific parameters and requirements.

