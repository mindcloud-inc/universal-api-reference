# CallKeeper: Update Contact

Updates an existing contact in CallKeeper.

```
PUT https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallKeeper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "page": 1,
      "page_size": 1,
      "status": "string",
      "total": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `id` | string | Resource identifier. |
| `items` | array<object> | Returned collection items. |
| `message` | string | Status or result message. |
| `page` | number | Current page number. |
| `page_size` | number | Page size. |
| `status` | string | Resource or operation status. |
| `total` | number | Total result count. |
| `updated_at` | date | Last update timestamp. |
| `url` | string | Returned URL when available. |

## Native endpoint

Through the native CallKeeper API, this operation is `PUT /contacts/:contact_id` (base URL `https://api.callkeeper.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

