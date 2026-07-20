# Click2Mail: Delete Addresses From List

Deletes addresses from a Click2Mail list.

```
DELETE https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/delete-addresses-from-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/delete-addresses-from-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/delete-addresses-from-list?${params}`, {
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
| `id[]` | array<number> | no | Require when other parameter addressType is null. Identify addresses to be deleted. |

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

Through the native Click2Mail API, this operation is `DELETE /molpro/addressLists` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-addresses-from-list.md) for the provider-specific parameters and requirements.

