# Click2Mail: List Account Addresses

Retrieves a list of account addresses from Click2Mail.

```
GET https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-account-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-account-addresses?connectionId=$CONNECTION_ID&addressType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "addressType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-account-addresses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressType` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |

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

Through the native Click2Mail API, this operation is `GET /molpro/account/addresses` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-addresses.md) for the provider-specific parameters and requirements.

