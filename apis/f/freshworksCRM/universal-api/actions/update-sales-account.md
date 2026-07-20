# Freshworks CRM: Update Sales Account

Updates an existing sales account in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-sales-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-sales-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-sales-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `salesAccount.customField` | object | no |  |
| `salesAccount.customField.cfDomainName` | string | no |  |
| `salesAccountId` | number | no | Unique sales account identifier. |
| `salesAccount` | object | no | Sales account fields to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sales_account": {
        "address": "string",
        "annual_revenue": 1,
        "avatar": "string",
        "city": "string",
        "country": "string",
        "custom_field": {
          "cf_domain_name": "Ava Chen"
        },
        "facebook": "string",
        "id": 1,
        "last_contacted": "2026-05-07T12:00:00.000Z",
        "last_contacted_mode": "string",
        "linkedin": "https://example.com",
        "links": {
          "conversations": "https://example.com"
        },
        "name": "Ava Chen",
        "number_of_employees": 1,
        "open_deals_amount": "string",
        "open_deals_count": 1,
        "phone": "string",
        "state": "string",
        "twitter": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "website": "string",
        "zipcode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sales_account.address` | string | Address. |
| `sales_account.annual_revenue` | number | Annual revenue. |
| `sales_account.avatar` | string | Avatar URL. |
| `sales_account.city` | string | City. |
| `sales_account.country` | string | Country. |
| `sales_account.custom_field.cf_domain_name` | string | Custom domain field. |
| `sales_account.facebook` | string | Facebook profile. |
| `sales_account.id` | number | Sales account identifier. |
| `sales_account.last_contacted` | date | Last contacted timestamp. |
| `sales_account.last_contacted_mode` | string | Last contact mode. |
| `sales_account.linkedin` | string | LinkedIn profile. |
| `sales_account.links.conversations` | string | Conversations link. |
| `sales_account.name` | string | Sales account name. |
| `sales_account.number_of_employees` | number | Number of employees. |
| `sales_account.open_deals_amount` | string | Open deals amount. |
| `sales_account.open_deals_count` | number | Open deals count. |
| `sales_account.phone` | string | Phone number. |
| `sales_account.state` | string | State. |
| `sales_account.twitter` | string | Twitter profile. |
| `sales_account.updated_at` | date | Updated timestamp. |
| `sales_account.website` | string | Website URL. |
| `sales_account.zipcode` | string | ZIP or postal code. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `PUT api/sales_accounts/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-account.md) for the provider-specific parameters and requirements.

