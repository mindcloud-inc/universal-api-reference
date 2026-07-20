# NetSuite - Basic: Get Purchase Order

Retrieves details for the purchase order in NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-purchase-order?${params}`, {
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
      "balance": 1,
      "billAddress": "string",
      "billingAddress": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "billingAddress_text": "string",
      "createdDate": "string",
      "currency": {
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
      "custbody_atlas_no_hdn": {
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
      "custbody_atlas_yes_hdn": {
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
      "custbody_bh_vendor_order_nbr": "string",
      "custbody_cs_pymt_inv_paymentreference": {
        "links": [
          {
            "href": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "custbody1": "string",
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
| `balance` | number |  |
| `billAddress` | string |  |
| `billingAddress` | object |  |
| `billingAddress_text` | string |  |
| `billingAddress.links` | array<object> |  |
| `billingAddress.links[].href` | string |  |
| `billingAddress.links[].method` | string |  |
| `billingAddress.links[].rel` | string |  |
| `createdDate` | string |  |
| `currency` | object |  |
| `currency.id` | string |  |
| `currency.links` | array<object> |  |
| `currency.links[].href` | string |  |
| `currency.links[].method` | string |  |
| `currency.links[].rel` | string |  |
| `currency.refName` | string |  |
| `custbody_atlas_no_hdn` | object |  |
| `custbody_atlas_no_hdn.id` | string |  |
| `custbody_atlas_no_hdn.links` | array<object> |  |
| `custbody_atlas_no_hdn.links[].href` | string |  |
| `custbody_atlas_no_hdn.links[].method` | string |  |
| `custbody_atlas_no_hdn.links[].rel` | string |  |
| `custbody_atlas_no_hdn.refName` | string |  |
| `custbody_atlas_yes_hdn` | object |  |
| `custbody_atlas_yes_hdn.id` | string |  |
| `custbody_atlas_yes_hdn.links` | array<object> |  |
| `custbody_atlas_yes_hdn.links[].href` | string |  |
| `custbody_atlas_yes_hdn.links[].method` | string |  |
| `custbody_atlas_yes_hdn.links[].rel` | string |  |
| `custbody_atlas_yes_hdn.refName` | string |  |
| `custbody_bh_vendor_order_nbr` | string |  |
| `custbody_cs_pymt_inv_paymentreference` | object |  |
| `custbody_cs_pymt_inv_paymentreference.links` | array<object> |  |
| `custbody_cs_pymt_inv_paymentreference.links[].href` | string |  |
| `custbody_cs_pymt_inv_paymentreference.links[].rel` | string |  |
| `custbody1` | string |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/purchaseOrder/:id` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.

