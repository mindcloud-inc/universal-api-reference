# GoDial: Create Contact

Creates a new contact in GoDial.

```
POST https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-add
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-add" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-add', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "dispo": "string",
      "email": "ava@example.com",
      "id": "string",
      "listId": "string",
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `dispo` | string |  |
| `email` | string |  |
| `id` | string |  |
| `listId` | string |  |
| `name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `POST /externals/contact/add` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/contact-add.md) for the provider-specific parameters and requirements.

