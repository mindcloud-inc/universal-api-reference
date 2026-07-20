# WEBLUCY: Update Contact

Updates an existing contact in WEBLUCY.

```
PUT https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "createdOn": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "note": "string",
      "phone": "string",
      "properties": [
        {}
      ],
      "state": "string",
      "subscribed": true,
      "subscriberLists": [
        1
      ],
      "tags": [
        "string"
      ],
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `createdOn` | number |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `note` | string |  |
| `phone` | string |  |
| `properties` | array<object> |  |
| `state` | string |  |
| `subscribed` | boolean |  |
| `subscriberLists` | array<number> |  |
| `tags` | array<string> |  |
| `zip` | string |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `PUT /contacts/{id}` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

