# Marketing Master IO: Create Contact

Creates a new contact in Marketing Master IO.

```
POST https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `book_ids[]` | array<string> | no | Array of contact book IDs to add the contact to. Accepts multiple values as an array. |
| `email` | string | no |  |
| `first_name` | string | no |  |
| `last_name` | string | no |  |
| `phone_number` | string | no |  |
| `subscriber` | boolean | yes | Set true to subscribe the contact or false to unsubscribe. |
| `tags[]` | array<string> | no | Array of tag IDs to apply to the contact. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `status` | boolean |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `POST /v1/contacts/list` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

