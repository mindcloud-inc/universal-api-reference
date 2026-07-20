# NetSuite - Basic: Get Estimate

Retrieves details for the estimate in NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-estimate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-estimate?${params}`, {
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
      "altShippingCost": 1,
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
      "canHaveStackable": true,
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
      "custbody_15699_exclude_from_ep_process": true,
      "custbody_atlas_exist_cust_hdn": {
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
      "custbody_atlas_hb_mm_exchange": true,
      "custbody_atlas_new_cust_hdn": {
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
      "custbody12": true,
      "custbody3": true,
      "custbody9": true,
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
| `altShippingCost` | number |  |
| `billAddress` | string |  |
| `billingAddress` | object |  |
| `billingAddress_text` | string |  |
| `billingAddress.links` | array<object> |  |
| `billingAddress.links[].href` | string |  |
| `billingAddress.links[].method` | string |  |
| `billingAddress.links[].rel` | string |  |
| `canHaveStackable` | boolean |  |
| `createdDate` | string |  |
| `currency` | object |  |
| `currency.id` | string |  |
| `currency.links` | array<object> |  |
| `currency.links[].href` | string |  |
| `currency.links[].method` | string |  |
| `currency.links[].rel` | string |  |
| `currency.refName` | string |  |
| `custbody_15699_exclude_from_ep_process` | boolean |  |
| `custbody_atlas_exist_cust_hdn` | object |  |
| `custbody_atlas_exist_cust_hdn.id` | string |  |
| `custbody_atlas_exist_cust_hdn.links` | array<object> |  |
| `custbody_atlas_exist_cust_hdn.links[].href` | string |  |
| `custbody_atlas_exist_cust_hdn.links[].method` | string |  |
| `custbody_atlas_exist_cust_hdn.links[].rel` | string |  |
| `custbody_atlas_exist_cust_hdn.refName` | string |  |
| `custbody_atlas_hb_mm_exchange` | boolean |  |
| `custbody_atlas_new_cust_hdn` | object |  |
| `custbody_atlas_new_cust_hdn.id` | string |  |
| `custbody_atlas_new_cust_hdn.links` | array<object> |  |
| `custbody_atlas_new_cust_hdn.links[].href` | string |  |
| `custbody_atlas_new_cust_hdn.links[].method` | string |  |
| `custbody_atlas_new_cust_hdn.links[].rel` | string |  |
| `custbody_atlas_new_cust_hdn.refName` | string |  |
| `custbody12` | boolean |  |
| `custbody3` | boolean |  |
| `custbody9` | boolean |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/estimate/:id` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-estimate.md) for the provider-specific parameters and requirements.

