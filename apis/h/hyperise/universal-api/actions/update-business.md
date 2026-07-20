# Hyperise: Update Business

Updates an existing business in Hyperise.

```
PUT https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/update-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/update-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/update-business', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes | The Hyperise business record ID. |
| `businessName` | string | no | Updated business name. |
| `email` | string | no | Updated business contact email. |
| `website` | string | no | Updated business website. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "updatedAt": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessName` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `updatedAt` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Hyperise API, this operation is `PUT /businesses/:businessId` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-business.md) for the provider-specific parameters and requirements.

