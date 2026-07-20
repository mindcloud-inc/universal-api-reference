# Click2Mail: Update Address Book Addresses

Updates addresses in a Click2Mail address book.

```
PUT https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-address-book-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-address-book-addresses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-address-book-addresses', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Address Book id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addresses` | object | no |  |
| `addressListName` | string | no |  |
| `addressMappingId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressListsInfo": [
        {}
      ],
      "count": 1,
      "description": "string",
      "id": 1,
      "status": 1,
      "statusLocation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressListsInfo` | array<object> |  |
| `count` | number |  |
| `description` | string |  |
| `id` | number |  |
| `status` | number |  |
| `statusLocation` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `PUT /molpro/addressBook/{id}/address` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-address-book-addresses.md) for the provider-specific parameters and requirements.

