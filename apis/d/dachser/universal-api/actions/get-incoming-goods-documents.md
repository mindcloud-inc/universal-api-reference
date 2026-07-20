# Dachser: Get Incoming Goods Documents

Retrieves incoming goods documents from Dachser.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-incoming-goods-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-incoming-goods-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-incoming-goods-documents?${params}`, {
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
| `incomingGoodsNumber` | string | no | Incoming goods number. |
| `orderNumber` | string | no | Order number. |
| `supplierNumber` | string | no | Supplier number. |
| `supplierReferenceNumber1` | string | no | First supplier reference number. |
| `supplierReferenceNumber2` | string | no | Second supplier reference number. |
| `date` | date | no | Incoming goods date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branchNumber` | number | no | DACHSER branch number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "id": "string",
      "incomingGoods": [
        {}
      ],
      "references": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> |  |
| `id` | string |  |
| `incomingGoods` | array<object> |  |
| `references` | array<object> |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/incominggoodsdocuments` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-incoming-goods-documents.md) for the provider-specific parameters and requirements.

