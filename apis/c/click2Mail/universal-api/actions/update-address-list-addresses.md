# Click2Mail: Update Address List Addresses

Updates addresses in a Click2Mail address list.

```
PUT https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-address-list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-address-list-addresses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-address-list-addresses', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseAddressListId` | number | no | Require when other parameter jobAddressListId is null. |
| `jobAddressListId` | number | no | Require when other parameter baseAddressListId is null. |
| `addresses` | object | no |  |
| `addressListName` | string | no |  |
| `addressMappingId` | string | no |  |

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

Through the native Click2Mail API, this operation is `PUT /molpro/addressLists/address2` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-address-list-addresses.md) for the provider-specific parameters and requirements.

