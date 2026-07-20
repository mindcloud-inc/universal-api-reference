# Click2Mail: Add Addresses From Address Book

Adds address book addresses to a Click2Mail address list.

```
POST https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/add-addresses-from-address-book
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/add-addresses-from-address-book" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/add-addresses-from-address-book', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | object | yes | array of address ids |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseAddressListId` | number | no | List ID to upadate |
| `jobAddressListId` | number | no | List ID to upadate |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `POST /molpro/addressLists/address/addressBook` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-addresses-from-address-book.md) for the provider-specific parameters and requirements.

