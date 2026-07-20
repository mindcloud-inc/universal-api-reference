# TikTok Shop: Get Authorized Shops



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-authorized-shops
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-authorized-shops?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-authorized-shops?${params}`, {
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
| `shopId` | string | no | (optional) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cipher": "string",
      "code": "string",
      "id": "string",
      "name": "Ava Chen",
      "region": "string",
      "sellerType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cipher` | string |  |
| `code` | string |  |
| `id` | string |  |
| `name` | string |  |
| `region` | string |  |
| `sellerType` | string |  |

## Native endpoint

Through the native TikTok Shop API, this operation is `GET https://open-api.tiktokglobalshop.com/authorization/202309/shops` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authorized-shops.md) for the provider-specific parameters and requirements.

