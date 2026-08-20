# Centerpoint: Get Product Template



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-product-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-product-template?connectionId=$CONNECTION_ID&PRODUCT_TEMPLATE_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PRODUCT_TEMPLATE_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-product-template?${params}`, {
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
| `PRODUCT_TEMPLATE_ID` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "accountId": 1,
        "corrected": "string",
        "correction": "string",
        "createdAt": "string",
        "deletedAt": {},
        "description": "string",
        "domain": "string",
        "externalId": "string",
        "fileId": {},
        "name": "Ava Chen",
        "unitCost": 1,
        "unitPrice": 1,
        "units": "string",
        "updatedAt": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.accountId` | number |  |
| `attributes.corrected` | string |  |
| `attributes.correction` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.description` | string |  |
| `attributes.domain` | string |  |
| `attributes.externalId` | string |  |
| `attributes.fileId` | object |  |
| `attributes.name` | string |  |
| `attributes.unitCost` | number |  |
| `attributes.unitPrice` | number |  |
| `attributes.units` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET product_templates/:PRODUCT_TEMPLATE_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-template.md) for the provider-specific parameters and requirements.

