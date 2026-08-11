# Shopify: Create Company



```
POST https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyName": "Acme Corporation",
  "externalId": "External company ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyName": "Acme Corporation",
    "externalId": "External company ID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyName` | string | yes | The Shopify B2B company name. Example: `Acme Corporation`. |
| `externalId` | string | yes | The external source-system ID stored in Shopify Company.externalId. Example: `External company ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "companyCreate": {
          "company": {
            "externalId": "string",
            "id": "string",
            "name": "Ava Chen"
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
| `data.companyCreate.company.externalId` | string | External source-system company ID |
| `data.companyCreate.company.id` | string | Shopify Company GID |
| `data.companyCreate.company.name` | string | Shopify company name |
| `data.companyCreate.userErrors[].code` | string | Shopify validation error code |
| `data.companyCreate.userErrors[].field` | array<string> | Input path associated with an error |
| `data.companyCreate.userErrors[].message` | string | Shopify validation error message |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

