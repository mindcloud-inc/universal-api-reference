# Campfire: Get User Info



```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/get-user-info?${params}`, {
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
      "country": "string",
      "customer_id": 1,
      "customer_name": "Ava Chen",
      "customer_type": "string",
      "deduct_credit_memos_from_invoiced_amount": true,
      "department_display_type": "string",
      "email": "ava@example.com",
      "entity_level_invoice_numbering": true,
      "exchange_rate_provider": "string",
      "first_name": "Ava",
      "fiscal_year_day": 1,
      "fiscal_year_month": 1,
      "invoice_message": "string",
      "last_name": "Chen",
      "name": "Ava Chen",
      "password_allowed": true,
      "root_currency": "string",
      "root_entity": 1,
      "root_entity_name": "Ava Chen",
      "show_alphanumeric_chart_accounts": true,
      "uncategorized_account": {
        "id": 1,
        "name": "Ava Chen"
      },
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `customer_id` | number |  |
| `customer_name` | string |  |
| `customer_type` | string |  |
| `deduct_credit_memos_from_invoiced_amount` | boolean |  |
| `department_display_type` | string |  |
| `email` | string |  |
| `entity_level_invoice_numbering` | boolean |  |
| `exchange_rate_provider` | string |  |
| `first_name` | string |  |
| `fiscal_year_day` | number |  |
| `fiscal_year_month` | number |  |
| `invoice_message` | string |  |
| `last_name` | string |  |
| `name` | string |  |
| `password_allowed` | boolean |  |
| `root_currency` | string |  |
| `root_entity` | number |  |
| `root_entity_name` | string |  |
| `show_alphanumeric_chart_accounts` | boolean |  |
| `uncategorized_account.id` | number |  |
| `uncategorized_account.name` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /users/api/get_user_info` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

