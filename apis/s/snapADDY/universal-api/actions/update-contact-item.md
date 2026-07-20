# snapADDY: Update Contact Item



```
PUT https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/update-contact-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/update-contact-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/update-contact-item', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        "string"
      ],
      "city": "string",
      "contactListId": "string",
      "country": "string",
      "created": "string",
      "customFields": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "organization": "string",
      "phone": "string",
      "position": "string",
      "updated": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<string> |  |
| `city` | string |  |
| `contactListId` | string |  |
| `country` | string |  |
| `created` | string |  |
| `customFields` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `organization` | string |  |
| `phone` | string |  |
| `position` | string |  |
| `updated` | string |  |
| `website` | string |  |

## Native endpoint

Through the native snapADDY API, this operation is `PUT /grabber/v1/contactitem/:itemId` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-item.md) for the provider-specific parameters and requirements.

