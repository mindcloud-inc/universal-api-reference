# redirect.pizza: Update Email Forward



```
PUT https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/update-email-forward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/update-email-forward" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/update-email-forward', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the email forward to update. |
| `destination` | string | yes | Destination email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "createdAt": "string",
      "destination": "string",
      "domain": "string",
      "id": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `createdAt` | string |  |
| `destination` | string |  |
| `domain` | string |  |
| `id` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `PUT /api/v1/email-forwards/{id}` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email-forward.md) for the provider-specific parameters and requirements.

