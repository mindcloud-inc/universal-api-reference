# NetSuite - Basic: Get Non-Inventory Sale Item

Retrieves details for the non-inventory sale item in NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-non-inventory-sale-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-non-inventory-sale-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-non-inventory-sale-item?${params}`, {
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
| `id` | string | no | Internal NetSuite record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": {
        "id": "string",
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ],
        "refName": "Ava Chen"
      },
      "correlatedItems": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "costCategory": {
        "id": "string",
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ],
        "refName": "Ava Chen"
      },
      "costEstimateType": {
        "id": "string",
        "links": [
          "https://example.com"
        ],
        "refName": "Ava Chen"
      },
      "createdDate": "string",
      "custitem1": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "custitem12": true,
      "custitem2": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "custitem3": {},
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "method": "https://example.com",
          "rel": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | object |  |
| `class.id` | string |  |
| `class.links` | array<object> |  |
| `class.links[].href` | string |  |
| `class.links[].method` | string |  |
| `class.links[].rel` | string |  |
| `class.refName` | string |  |
| `correlatedItems` | object |  |
| `correlatedItems.links` | array<object> |  |
| `correlatedItems.links[].href` | string |  |
| `correlatedItems.links[].method` | string |  |
| `correlatedItems.links[].rel` | string |  |
| `costCategory` | object |  |
| `costCategory.id` | string |  |
| `costCategory.links` | array<object> |  |
| `costCategory.links[].href` | string |  |
| `costCategory.links[].method` | string |  |
| `costCategory.links[].rel` | string |  |
| `costCategory.refName` | string |  |
| `costEstimateType` | object |  |
| `costEstimateType.id` | string |  |
| `costEstimateType.links` | array<string> |  |
| `costEstimateType.refName` | string |  |
| `createdDate` | string |  |
| `custitem1` | object |  |
| `custitem1.links` | array<object> |  |
| `custitem1.links[].href` | string |  |
| `custitem1.links[].method` | string |  |
| `custitem1.links[].rel` | string |  |
| `custitem12` | boolean |  |
| `custitem2` | object |  |
| `custitem2.links` | array<object> |  |
| `custitem2.links[].href` | string |  |
| `custitem2.links[].method` | string |  |
| `custitem2.links[].rel` | string |  |
| `custitem3` | object |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/nonInventorySaleItem/:id` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-non-inventory-sale-item.md) for the provider-specific parameters and requirements.

