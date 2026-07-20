# Jostle: Set User Status



```
PUT https://connect.mindcloud.co/v1/universal/jostle/latest/actions/set-user-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jostle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/set-user-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user.userId": "string",
  "type": "string",
  "resetAfter": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jostle/latest/actions/set-user-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user.userId": "string",
    "type": "string",
    "resetAfter": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user.userId` | string | yes | Id of the user |
| `type` | string | yes | The type of user status |
| `resetAfter` | string | yes | When the user status should clear itself |
| `statusMessage` | string | no | User-specified status message when type is CUSTOM |
| `emoji` | string | no | User-specified emoji when type is CUSTOM |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "resetInterval": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `resetInterval` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Jostle API, this operation is `POST /v2/people/status` (base URL `https://api-prod.jostle.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-user-status.md) for the provider-specific parameters and requirements.

