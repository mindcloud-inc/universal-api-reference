# CATS: Get Site

Retrieves site details from the CATS account.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-site?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultCompanyId": 1,
      "Embedded": {
        "defaultCompany": {
          "address": {
            "city": {},
            "postalCode": {},
            "state": {},
            "street": {}
          },
          "billingContactId": {},
          "countryCode": {},
          "dateCreated": "string",
          "dateModified": "string",
          "enteredById": 1,
          "id": 1,
          "isHot": true,
          "keyTechnologies": {},
          "Links": {
            "self": {
              "href": "https://example.com"
            }
          },
          "name": "Ava Chen",
          "notes": "string",
          "ownerId": 1,
          "phones": {
            "fax": {},
            "primary": {},
            "secondary": {}
          },
          "statusId": 1,
          "website": {}
        },
        "users": [
          {
            "firstName": "Ava",
            "id": 1,
            "lastName": "Chen",
            "Links": {
              "self": {
                "href": "https://example.com"
              }
            },
            "title": "string",
            "username": "Ava Chen"
          }
        ]
      },
      "id": 1,
      "Links": {
        "defaultCompany": {
          "href": "https://example.com"
        },
        "self": {
          "href": "https://example.com"
        },
        "users": {
          "href": "https://example.com"
        }
      },
      "mode": "string",
      "subdomain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultCompanyId` | number |  |
| `Embedded.defaultCompany.address.city` | object |  |
| `Embedded.defaultCompany.address.postalCode` | object |  |
| `Embedded.defaultCompany.address.state` | object |  |
| `Embedded.defaultCompany.address.street` | object |  |
| `Embedded.defaultCompany.billingContactId` | object |  |
| `Embedded.defaultCompany.countryCode` | object |  |
| `Embedded.defaultCompany.dateCreated` | string |  |
| `Embedded.defaultCompany.dateModified` | string |  |
| `Embedded.defaultCompany.enteredById` | number |  |
| `Embedded.defaultCompany.id` | number |  |
| `Embedded.defaultCompany.isHot` | boolean |  |
| `Embedded.defaultCompany.keyTechnologies` | object |  |
| `Embedded.defaultCompany.Links.self.href` | string |  |
| `Embedded.defaultCompany.name` | string |  |
| `Embedded.defaultCompany.notes` | string |  |
| `Embedded.defaultCompany.ownerId` | number |  |
| `Embedded.defaultCompany.phones.fax` | object |  |
| `Embedded.defaultCompany.phones.primary` | object |  |
| `Embedded.defaultCompany.phones.secondary` | object |  |
| `Embedded.defaultCompany.statusId` | number |  |
| `Embedded.defaultCompany.website` | object |  |
| `Embedded.users[].firstName` | string |  |
| `Embedded.users[].id` | number |  |
| `Embedded.users[].lastName` | string |  |
| `Embedded.users[].Links.self.href` | string |  |
| `Embedded.users[].title` | string |  |
| `Embedded.users[].username` | string |  |
| `id` | number |  |
| `Links.defaultCompany.href` | string |  |
| `Links.self.href` | string |  |
| `Links.users.href` | string |  |
| `mode` | string |  |
| `subdomain` | string |  |

## Native endpoint

Through the native CATS API, this operation is `GET /site` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

