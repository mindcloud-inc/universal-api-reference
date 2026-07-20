# NetSuite - Basic: Get Vendor

Retrieves details for the vendor in NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-vendor?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-vendor?${params}`, {
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
      "addressBook": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "autoName": true,
      "balance": 1,
      "balancePrimary": 1,
      "campaigns": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "contactList": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "custentity_11724_pay_bank_fees": true,
      "custentity_2663_payment_method": true,
      "custentity5": true,
      "customForm": {
        "id": "string",
        "links": [
          "https://example.com"
        ],
        "refName": "Ava Chen"
      },
      "dateCreated": "string",
      "emailPreference": {
        "id": "ava@example.com",
        "links": [
          "ava@example.com"
        ],
        "refName": "ava@example.com"
      },
      "emailTransactions": true,
      "entityId": "string",
      "faxTransactions": true,
      "globalSubscriptionStatus": {
        "id": "string",
        "links": [
          "https://example.com"
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
| `addressBook` | object |  |
| `addressBook.links` | array<object> |  |
| `addressBook.links[].href` | string |  |
| `addressBook.links[].method` | string |  |
| `addressBook.links[].rel` | string |  |
| `autoName` | boolean |  |
| `balance` | number |  |
| `balancePrimary` | number |  |
| `campaigns` | object |  |
| `campaigns.links` | array<object> |  |
| `campaigns.links[].href` | string |  |
| `campaigns.links[].method` | string |  |
| `campaigns.links[].rel` | string |  |
| `contactList` | object |  |
| `contactList.links` | array<object> |  |
| `contactList.links[].href` | string |  |
| `contactList.links[].method` | string |  |
| `contactList.links[].rel` | string |  |
| `custentity_11724_pay_bank_fees` | boolean |  |
| `custentity_2663_payment_method` | boolean |  |
| `custentity5` | boolean |  |
| `customForm` | object |  |
| `customForm.id` | string |  |
| `customForm.links` | array<string> |  |
| `customForm.refName` | string |  |
| `dateCreated` | string |  |
| `emailPreference` | object |  |
| `emailPreference.id` | string |  |
| `emailPreference.links` | array<string> |  |
| `emailPreference.refName` | string |  |
| `emailTransactions` | boolean |  |
| `entityId` | string |  |
| `faxTransactions` | boolean |  |
| `globalSubscriptionStatus` | object |  |
| `globalSubscriptionStatus.id` | string |  |
| `globalSubscriptionStatus.links` | array<string> |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/vendor/:id` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor.md) for the provider-specific parameters and requirements.

