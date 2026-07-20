# Rakuten Advertising: List coupon metadata

Retrieves coupon metadata from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-coupon-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-coupon-metadata?connectionId=$CONNECTION_ID&promocat=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "promocat": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-coupon-metadata?${params}`, {
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
| `promocat` | string | yes | Set to 1 to retrieve coupon network, category, and promotion type metadata. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "categoryName": "Ava Chen",
      "networkId": "string",
      "networkName": "Ava Chen",
      "promotionTypeId": "string",
      "promotionTypeName": "Ava Chen",
      "rawXml": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string | Coupon category ID. |
| `categoryName` | string | Coupon category name. |
| `networkId` | string | Coupon metadata network ID. |
| `networkName` | string | Coupon metadata network name. |
| `promotionTypeId` | string | Coupon promotion type ID. |
| `promotionTypeName` | string | Coupon promotion type name. |
| `rawXml` | string | Raw coupon metadata XML when returned by the API. |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /coupon/1.0` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-coupon-metadata.md) for the provider-specific parameters and requirements.

