# NetSuite - Basic: Get Customer

Retrieves details for the customer in NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-customer?${params}`, {
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
      "accessRole": {
        "id": "string",
        "links": [
          "https://example.com"
        ],
        "refName": "Ava Chen"
      },
      "addressBook": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "aging": 1,
      "aging1": 1,
      "aging2": 1,
      "aging3": 1,
      "aging4": 1,
      "alcoholRecipientType": {
        "id": "string",
        "links": [
          "https://example.com"
        ],
        "refName": "Ava Chen"
      },
      "balance": 1,
      "campaigns": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "category": {
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
      "companyName": "Ava Chen",
      "consolAging": 1,
      "consolAging1": 1,
      "consolAging2": 1,
      "consolAging3": 1,
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
| `accessRole` | object |  |
| `accessRole.id` | string |  |
| `accessRole.links` | array<string> |  |
| `accessRole.refName` | string |  |
| `addressBook` | object |  |
| `addressBook.links` | array<object> |  |
| `addressBook.links[].href` | string |  |
| `addressBook.links[].method` | string |  |
| `addressBook.links[].rel` | string |  |
| `aging` | number |  |
| `aging1` | number |  |
| `aging2` | number |  |
| `aging3` | number |  |
| `aging4` | number |  |
| `alcoholRecipientType` | object |  |
| `alcoholRecipientType.id` | string |  |
| `alcoholRecipientType.links` | array<string> |  |
| `alcoholRecipientType.refName` | string |  |
| `balance` | number |  |
| `campaigns` | object |  |
| `campaigns.links` | array<object> |  |
| `campaigns.links[].href` | string |  |
| `campaigns.links[].method` | string |  |
| `campaigns.links[].rel` | string |  |
| `category` | object |  |
| `category.id` | string |  |
| `category.links` | array<object> |  |
| `category.links[].href` | string |  |
| `category.links[].method` | string |  |
| `category.links[].rel` | string |  |
| `category.refName` | string |  |
| `companyName` | string |  |
| `consolAging` | number |  |
| `consolAging1` | number |  |
| `consolAging2` | number |  |
| `consolAging3` | number |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/customer/:id` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

