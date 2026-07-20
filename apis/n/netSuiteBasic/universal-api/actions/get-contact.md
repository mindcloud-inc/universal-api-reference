# NetSuite - Basic: Get Contact

Retrieves details for the contact in NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-contact?${params}`, {
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
      "category": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "company": {
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
      "custentity_esc_last_modified_date": "string",
      "custentitypersonalusecheck": true,
      "custentityprofessional_accounts_amazon": true,
      "custentityprofessional_accounts_insta": true,
      "custentityprofessional_accounts_linkedin": true,
      "custentityprofessional_accounts_select": {
        "links": [
          {
            "href": "https://example.com",
            "method": "https://example.com",
            "rel": "https://example.com"
          }
        ]
      },
      "custentityprofessional_accounts_twitter": true,
      "custentityprofessionalaccount_fb": true,
      "custentityreselling_gyms_clubs": true,
      "custentityreselling_marketplace": true,
      "custentityreselling_onlinestore": true,
      "custentityreselling_other": true,
      "custentityreselling_practitioner": true,
      "custentityreselling_retail": true,
      "custentitywebsitecheck": true,
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
| `category` | object |  |
| `category.links` | array<object> |  |
| `category.links[].href` | string |  |
| `category.links[].method` | string |  |
| `category.links[].rel` | string |  |
| `company` | object |  |
| `company.id` | string |  |
| `company.links` | array<object> |  |
| `company.links[].href` | string |  |
| `company.links[].method` | string |  |
| `company.links[].rel` | string |  |
| `company.refName` | string |  |
| `custentity_esc_last_modified_date` | string |  |
| `custentitypersonalusecheck` | boolean |  |
| `custentityprofessional_accounts_amazon` | boolean |  |
| `custentityprofessional_accounts_insta` | boolean |  |
| `custentityprofessional_accounts_linkedin` | boolean |  |
| `custentityprofessional_accounts_select` | object |  |
| `custentityprofessional_accounts_select.links` | array<object> |  |
| `custentityprofessional_accounts_select.links[].href` | string |  |
| `custentityprofessional_accounts_select.links[].method` | string |  |
| `custentityprofessional_accounts_select.links[].rel` | string |  |
| `custentityprofessional_accounts_twitter` | boolean |  |
| `custentityprofessionalaccount_fb` | boolean |  |
| `custentityreselling_gyms_clubs` | boolean |  |
| `custentityreselling_marketplace` | boolean |  |
| `custentityreselling_onlinestore` | boolean |  |
| `custentityreselling_other` | boolean |  |
| `custentityreselling_practitioner` | boolean |  |
| `custentityreselling_retail` | boolean |  |
| `custentitywebsitecheck` | boolean |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/contact/:id` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

