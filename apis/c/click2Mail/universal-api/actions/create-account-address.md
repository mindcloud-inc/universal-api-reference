# Click2Mail: Create Account Address

Creates a new account address in Click2Mail.

```
POST https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/create-account-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/create-account-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "description": "string",
  "address1": "string",
  "city": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/create-account-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "description": "string",
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
| `type` | string | yes |  |
| `description` | string | yes |  |
| `address1` | string | yes |  |
| `city` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prefix` | string | no |  |
| `suffix` | string | no |  |
| `makeDefault` | string | no |  |
| `firstName` | string | no |  |
| `middleName` | string | no |  |
| `lastName` | string | no |  |
| `address2` | string | no |  |
| `address3` | string | no |  |
| `state` | string | no |  |
| `zip` | string | no |  |
| `phone` | string | no |  |
| `permitNumber` | string | no |  |
| `replyCity` | string | no |  |
| `replyRegionId` | string | no |  |
| `organization` | string | no |  |
| `country` | string | no |  |

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

Through the native Click2Mail API, this operation is `POST /molpro/account/addresses` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account-address.md) for the provider-specific parameters and requirements.

