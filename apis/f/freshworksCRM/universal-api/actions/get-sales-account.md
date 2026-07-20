# Freshworks CRM: Get Sales Account

Retrieves a sales account from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-sales-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-sales-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-sales-account?${params}`, {
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
| `salesAccountId` | number | no | Unique sales account identifier. |

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
        "owner_id": 1,
        "phone": "string",
        "state": "string",
        "twitter": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "website": "string",
        "zipcode": "string"
      },
      "users": [
        {
          "display_name": "Ava Chen",
          "email": "ava@example.com",
          "id": 1
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
| `sales_account.owner_id` | number | Owner user id. |
| `sales_account.phone` | string | Phone number. |
| `sales_account.state` | string | State. |
| `sales_account.twitter` | string | Twitter profile. |
| `sales_account.updated_at` | date | Updated timestamp. |
| `sales_account.website` | string | Website URL. |
| `sales_account.zipcode` | string | ZIP or postal code. |
| `users[].display_name` | string | Related user display name. |
| `users[].email` | string | Related user email. |
| `users[].id` | number | Related user id. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET api/sales_accounts/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-account.md) for the provider-specific parameters and requirements.

