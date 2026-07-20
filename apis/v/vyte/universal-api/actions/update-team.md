# Vyte: Update Team

Updates an existing team in Vyte.

```
PUT https://connect.mindcloud.co/v1/universal/vyte/latest/actions/update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vyte/latest/actions/update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native Vyte API, this operation is `PUT v2/teams/:team_id` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team.md) for the provider-specific parameters and requirements.

