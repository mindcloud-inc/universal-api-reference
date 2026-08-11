# Shopify: Create Company Contact



```
POST https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-company-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-company-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "gid://shopify/Company/123456789",
  "email": "person@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-company-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "gid://shopify/Company/123456789",
    "email": "person@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | Shopify Company GID that the contact belongs to. Example: `gid://shopify/Company/123456789`. |
| `email` | string | yes | Email address for the new company contact and associated customer. Example: `person@example.com`. |
| `firstName` | string | no | First name for the company contact. Example: `Avery`. |
| `lastName` | string | no | Last name for the company contact. Example: `Brown`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "companyContactCreate": {
          "companyContact": {
            "company": {
              "externalId": "string",
              "id": "string",
              "name": "Ava Chen"
            },
            "customer": {
              "email": "ava@example.com",
              "firstName": "Ava",
              "id": "string",
              "lastName": "Chen"
            },
            "id": "string"
          },
          "userErrors": [
            {
              "code": "string",
              "field": [
                "string"
              ],
              "message": "string"
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.companyContactCreate.companyContact.company.externalId` | string | External source-system company ID |
| `data.companyContactCreate.companyContact.company.id` | string | Shopify Company GID |
| `data.companyContactCreate.companyContact.company.name` | string | Shopify company name |
| `data.companyContactCreate.companyContact.customer.email` | string | Customer email |
| `data.companyContactCreate.companyContact.customer.firstName` | string | Customer first name |
| `data.companyContactCreate.companyContact.customer.id` | string | Created Shopify Customer GID |
| `data.companyContactCreate.companyContact.customer.lastName` | string | Customer last name |
| `data.companyContactCreate.companyContact.id` | string | Shopify CompanyContact GID |
| `data.companyContactCreate.userErrors[].code` | string | Shopify validation error code |
| `data.companyContactCreate.userErrors[].field` | array<string> | Input path associated with an error |
| `data.companyContactCreate.userErrors[].message` | string | Shopify validation error message |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company-contact.md) for the provider-specific parameters and requirements.

