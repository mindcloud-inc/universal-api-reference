# Temu: List Local SKUs

Search the local SKU list

```
GET https://connect.mindcloud.co/v1/universal/temu/latest/actions/list-local-sk-us
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temu/latest/actions/list-local-sk-us?connectionId=$CONNECTION_ID&skuSearchType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "skuSearchType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temu/latest/actions/list-local-sk-us?${params}`, {
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
| `skuSearchType` | list<string> | yes | SKU status filter |
| `goodsName` | string | no |  |
| `goodsSearchTags` | list<number> | no | Optional. **Goods search tags:** 1 - Low traffic 4 - Restricted traffic Accepts multiple values as an array. |
| `catIdList` | string | no | Category id for search limit of 100 Accepts multiple values as an array. |
| `skuIdList` | string | no | Sku ID for search limit of 200 Accepts multiple values as an array. |
| `goodsIdList` | string | no | Product ID for search limit of 100 Accepts multiple values as an array. |
| `outSkuSnList` | string | no | OutSkuSn for search limit of 200 Accepts multiple values as an array. |
| `outGoodsSnList` | string | no | OutGoodsSn for search limit of 100 Accepts multiple values as an array. |
| `goodsCreateTimeFrom` | date | no |  |
| `goodsCreateTimeTo` | date | no |  |
| `skuStatusChangeTimeFrom` | date | no |  |
| `skuStatusChangeTimeTo` | date | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderField` | string | no | Default: `create_time`. |
| `orderType` | list<number> | no | Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "catId": "string",
      "catType": 1,
      "goodsCreateTime": "2026-05-07T12:00:00.000Z",
      "goodsId": "string",
      "goodsName": "Ava Chen",
      "lowTrafficTag": 1,
      "outGoodsSn": "string",
      "outSkuSn": "string",
      "restrictedTrafficTag": 1,
      "skuId": "string",
      "skuStatus": "string",
      "skuStatusChangeTime": "2026-05-07T12:00:00.000Z",
      "skuSubStatus": "string",
      "specList": [
        {
          "parentSpecId": 1,
          "specId": 1
        }
      ],
      "specName": "Ava Chen",
      "thumbUrl": "https://example.com",
      "volumeInfo": {
        "height": "string",
        "length": "string",
        "unit": "string",
        "width": "string"
      },
      "weightInfo": {
        "unit": "string",
        "weight": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catId` | string |  |
| `catType` | number |  |
| `goodsCreateTime` | date |  |
| `goodsId` | string |  |
| `goodsName` | string |  |
| `lowTrafficTag` | number |  |
| `outGoodsSn` | string |  |
| `outSkuSn` | string |  |
| `restrictedTrafficTag` | number |  |
| `skuId` | string |  |
| `skuStatus` | string |  |
| `skuStatusChangeTime` | date |  |
| `skuSubStatus` | string |  |
| `specList[].parentSpecId` | number |  |
| `specList[].specId` | number |  |
| `specName` | string |  |
| `thumbUrl` | string |  |
| `volumeInfo.height` | string |  |
| `volumeInfo.length` | string |  |
| `volumeInfo.unit` | string |  |
| `volumeInfo.width` | string |  |
| `weightInfo.unit` | string |  |
| `weightInfo.weight` | string |  |

## Native endpoint

Through the native Temu API, this operation is `POST /router` (base URL `https://openapi-b-us.temu.com/openapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-local-sk-us.md) for the provider-specific parameters and requirements.

