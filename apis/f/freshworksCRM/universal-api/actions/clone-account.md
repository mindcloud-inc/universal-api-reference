# Freshworks CRM: Clone Account

Creates a sales account by cloning one in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "salesAccount": {},
  "salesAccount.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "salesAccount": {},
    "salesAccount.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `salesAccount` | object | yes |  |
| `salesAccount.name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sales_account": {
        "has_connections": true,
        "id": 1,
        "name": "Ava Chen",
        "owner_id": 1,
        "record_type_id": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sales_account` | object |  |
| `sales_account.has_connections` | boolean |  |
| `sales_account.id` | number |  |
| `sales_account.name` | string |  |
| `sales_account.owner_id` | number |  |
| `sales_account.record_type_id` | string |  |
| `sales_account.updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/sales_accounts/:id/clone` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clone-account.md) for the provider-specific parameters and requirements.

