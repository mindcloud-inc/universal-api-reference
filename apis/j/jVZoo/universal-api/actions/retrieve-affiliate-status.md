# JVZoo: Retrieve Affiliate Status

Retrieves affiliate status for a JVZoo product.

```
GET https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/retrieve-affiliate-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JVZoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/retrieve-affiliate-status?connectionId=$CONNECTION_ID&affiliateId=1&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "affiliateId": "1",
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/retrieve-affiliate-status?${params}`, {
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
| `affiliateId` | number | yes | The ID of the affiliate. |
| `productId` | number | yes | The ID of the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": "string",
      "comments": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "customCommission": "string",
      "delayedCommission": "string",
      "productId": 1,
      "statusId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | string | Affiliate ID. |
| `comments` | string | Relationship comments. |
| `created` | date | When the affiliate relationship was created. |
| `customCommission` | string | Custom commission rate. |
| `delayedCommission` | string | Delayed commission value. |
| `productId` | number | Product ID. |
| `statusId` | number | Affiliate status ID. |

## Native endpoint

Through the native JVZoo API, this operation is `GET /products/:product_id/affiliates/:affiliate_id` (base URL `https://api.jvzoo.com/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-affiliate-status.md) for the provider-specific parameters and requirements.

