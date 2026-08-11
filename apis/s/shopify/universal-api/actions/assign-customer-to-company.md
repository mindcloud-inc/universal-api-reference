# Shopify: Assign Customer to Company



```
PUT https://connect.mindcloud.co/v1/universal/shopify/latest/actions/assign-customer-to-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/assign-customer-to-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "gid://shopify/Company/123456789",
  "customerId": "gid://shopify/Customer/123456789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/assign-customer-to-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "gid://shopify/Company/123456789",
    "customerId": "gid://shopify/Customer/123456789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | Shopify Company GID to receive the existing customer. Example: `gid://shopify/Company/123456789`. |
| `customerId` | string | yes | Shopify Customer GID to assign as a company contact. Example: `gid://shopify/Customer/123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "companyAssignCustomerAsContact": {
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
| `data.companyAssignCustomerAsContact.companyContact.company.externalId` | string | External source-system company ID |
| `data.companyAssignCustomerAsContact.companyContact.company.id` | string | Shopify Company GID |
| `data.companyAssignCustomerAsContact.companyContact.company.name` | string | Shopify company name |
| `data.companyAssignCustomerAsContact.companyContact.customer.email` | string | Customer email |
| `data.companyAssignCustomerAsContact.companyContact.customer.firstName` | string | Customer first name |
| `data.companyAssignCustomerAsContact.companyContact.customer.id` | string | Assigned Shopify Customer GID |
| `data.companyAssignCustomerAsContact.companyContact.customer.lastName` | string | Customer last name |
| `data.companyAssignCustomerAsContact.companyContact.id` | string | Shopify CompanyContact GID |
| `data.companyAssignCustomerAsContact.userErrors[].code` | string | Shopify validation error code |
| `data.companyAssignCustomerAsContact.userErrors[].field` | array<string> | Input path associated with an error |
| `data.companyAssignCustomerAsContact.userErrors[].message` | string | Shopify validation error message |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-customer-to-company.md) for the provider-specific parameters and requirements.

