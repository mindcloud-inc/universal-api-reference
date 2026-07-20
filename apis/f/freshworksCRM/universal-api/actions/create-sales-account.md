# Freshworks CRM: Create Sales Account

Creates a new sales account in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-sales-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-sales-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-sales-account', {
  method: 'POST',
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
| `salesAccount` | object | no | Sales account payload object as documented by Freshworks CRM. |
| `salesAccount.customField` | object | no |  |
| `salesAccount.customField.cfDomainName` | string | no |  |
| `salesAccount.name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sales_account": {
        "child_sales_accounts_count": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "has_connections": true,
        "id": 1,
        "is_deleted": true,
        "links": {
          "conversations": "https://example.com"
        },
        "name": "Ava Chen",
        "parent_sales_account_id": 1,
        "phone": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "website": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sales_account.child_sales_accounts_count` | number |  |
| `sales_account.created_at` | date |  |
| `sales_account.has_connections` | boolean |  |
| `sales_account.id` | number |  |
| `sales_account.is_deleted` | boolean |  |
| `sales_account.links.conversations` | string |  |
| `sales_account.name` | string |  |
| `sales_account.parent_sales_account_id` | number |  |
| `sales_account.phone` | string |  |
| `sales_account.updated_at` | date |  |
| `sales_account.website` | string |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST api/sales_accounts` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-account.md) for the provider-specific parameters and requirements.

