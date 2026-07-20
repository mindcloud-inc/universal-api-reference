# NetSuite - Basic: Get Inventory Item

Retrieves details for the inventory item in NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-inventory-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-inventory-item?${params}`, {
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
      "assetAccount": {
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
      "atpMethod": {
        "id": "string",
        "links": [
          "https://example.com"
        ],
        "refName": "Ava Chen"
      },
      "autoLeadTime": true,
      "autoPreferredStockLevel": true,
      "autoReorderPoint": true,
      "binNumber": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
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
      "cogsAccount": {
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
      "copyDescription": true,
      "correlatedItems": {
        "links": [
          {}
        ]
      },
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
| `assetAccount` | object |  |
| `assetAccount.id` | string |  |
| `assetAccount.links` | array<object> |  |
| `assetAccount.links[].href` | string |  |
| `assetAccount.links[].method` | string |  |
| `assetAccount.links[].rel` | string |  |
| `assetAccount.refName` | string |  |
| `atpMethod` | object |  |
| `atpMethod.id` | string |  |
| `atpMethod.links` | array<string> |  |
| `atpMethod.refName` | string |  |
| `autoLeadTime` | boolean |  |
| `autoPreferredStockLevel` | boolean |  |
| `autoReorderPoint` | boolean |  |
| `binNumber` | object |  |
| `binNumber.links` | array<object> |  |
| `binNumber.links[].href` | string |  |
| `binNumber.links[].method` | string |  |
| `binNumber.links[].rel` | string |  |
| `class` | object |  |
| `class.id` | string |  |
| `class.links` | array<object> |  |
| `class.links[].href` | string |  |
| `class.links[].method` | string |  |
| `class.links[].rel` | string |  |
| `class.refName` | string |  |
| `cogsAccount` | object |  |
| `cogsAccount.id` | string |  |
| `cogsAccount.links` | array<object> |  |
| `cogsAccount.links[].href` | string |  |
| `cogsAccount.links[].method` | string |  |
| `cogsAccount.links[].rel` | string |  |
| `cogsAccount.refName` | string |  |
| `copyDescription` | boolean |  |
| `correlatedItems` | object |  |
| `correlatedItems.links` | array<object> |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/inventoryItem/:id` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-item.md) for the provider-specific parameters and requirements.

