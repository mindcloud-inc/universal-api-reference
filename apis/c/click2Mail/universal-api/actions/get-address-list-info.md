# Click2Mail: Get Address List Info

Retrieves address list metadata from Click2Mail.

```
GET https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-address-list-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-address-list-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-address-list-info?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressType` | string | no | Use for filtering addresses. |
| `baseAddressListId` | number | no | Require when other parameter jobAddressListId is null. |
| `jobAddressListId` | number | no | Require when other parameter baseAddressListId is null. |
| `offset` | number | no | Use for filtering addresses. |
| `limit` | number | no | Integer referring number of addresses to be return. Default is 10. Default: `10`. |

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

Through the native Click2Mail API, this operation is `GET /molpro/addressLists/info` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address-list-info.md) for the provider-specific parameters and requirements.

