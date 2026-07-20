# Click2Mail: Update Account Address

Updates an existing account address in Click2Mail.

```
PUT https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-account-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-account-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addressId": "string",
  "description": "string",
  "type": "string",
  "address1": "string",
  "city": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/update-account-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addressId": "string",
    "description": "string",
    "type": "string",
    "address1": "string",
    "city": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressId` | string | yes |  |
| `description` | string | yes | The name to identify this address |
| `type` | string | yes |  |
| `address1` | string | yes | Address line 1 |
| `city` | string | yes | City |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `makeDefault` | string | no | A Yes indicates that this address is to be made the default address in this type |
| `prefix` | string | no |  |
| `firstName` | string | no | First Name |
| `middleName` | string | no | Middle Initial |
| `lastName` | string | no | Last Name |
| `suffix` | string | no |  |
| `address2` | string | no | Address line 2 |
| `address3` | string | no | Address line 3 |
| `state` | string | no | State |
| `zip` | string | no | Postal Code |
| `phone` | string | no | Contract phone number for this address. Required for EDDM mailer address, Must be properly formatted. For example XXX-XXX-XXXX or XXX-XXX-XXXX ext XXXX format. |
| `permitNumber` | string | no | Required for Business Reply address |
| `replyCity` | string | no | Required for Business Reply addresses |
| `replyRegionId` | string | no | Required for Business Reply address |
| `organization` | string | no | Company Name |
| `country` | string | no | country |

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

Through the native Click2Mail API, this operation is `POST /molpro/account/addresses/{addressId}` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-address.md) for the provider-specific parameters and requirements.

