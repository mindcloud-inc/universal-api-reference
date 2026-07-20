# Vyte: Set User Availabilities

Sets a user's availabilities in Vyte.

```
POST https://connect.mindcloud.co/v1/universal/vyte/latest/actions/set-user-availabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/set-user-availabilities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vyte/latest/actions/set-user-availabilities', {
  method: 'POST',
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
| `userId` | string | no | The Vyte user ID. Default: `69ca9fead310017cb903a0fd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "belongs_to": "string",
      "days": {},
      "organization": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `belongs_to` | string |  |
| `days` | object |  |
| `organization` | string |  |

## Native endpoint

Through the native Vyte API, this operation is `POST v2/users/:user_id/availabilities` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-user-availabilities.md) for the provider-specific parameters and requirements.

