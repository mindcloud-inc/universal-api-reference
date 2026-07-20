# Bluebarry: Get Product

Retrieves a single product from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-product?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clonedFrom": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "groupId": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "inactive": true,
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifierId": "string",
      "name": "Ava Chen",
      "productCheckAdvisor": "string",
      "productCheckAdvisorId": "string",
      "productProperties": [
        {}
      ],
      "productTexts": [
        {}
      ],
      "reference": "string",
      "syncedFromLiveProductFeed": "string",
      "syncedFromLiveProductFeedId": "string",
      "tenant": "string",
      "tenantId": "string",
      "url": "https://example.com",
      "variantIconImageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clonedFrom` | string |  |
| `createdDate` | date |  |
| `creatorId` | string |  |
| `groupId` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `inactive` | boolean |  |
| `modifiedDate` | date |  |
| `modifierId` | string |  |
| `name` | string |  |
| `productCheckAdvisor` | string |  |
| `productCheckAdvisorId` | string |  |
| `productProperties` | array<object> |  |
| `productTexts` | array<object> |  |
| `reference` | string |  |
| `syncedFromLiveProductFeed` | string |  |
| `syncedFromLiveProductFeedId` | string |  |
| `tenant` | string |  |
| `tenantId` | string |  |
| `url` | string |  |
| `variantIconImageUrl` | string |  |

## Native endpoint

Through the native Bluebarry API, this operation is `GET /data/Products({id})` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

