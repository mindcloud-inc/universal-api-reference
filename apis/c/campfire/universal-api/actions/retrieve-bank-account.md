# Campfire: Retrieve Bank Account

Retrieves a bank account from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-bank-account?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-bank-account?${params}`, {
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
| `id` | number | yes | The bank account ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_subtype": "string",
      "account_type": "string",
      "available_balance": 1,
      "chart_of_accounts_account": 1,
      "chart_of_accounts_account_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "current_balance": 1,
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "department": 1,
      "department_name": "Ava Chen",
      "entity": 1,
      "entity_name": "Ava Chen",
      "external_account_id": "string",
      "id": 1,
      "institution_id": "string",
      "is_deleted": true,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nickname": "Ava Chen",
      "source": "string",
      "status": "string",
      "tags": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_subtype` | string |  |
| `account_type` | string |  |
| `available_balance` | number |  |
| `chart_of_accounts_account` | number |  |
| `chart_of_accounts_account_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `current_balance` | number |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `department` | number |  |
| `department_name` | string |  |
| `entity` | number |  |
| `entity_name` | string |  |
| `external_account_id` | string |  |
| `id` | number |  |
| `institution_id` | string |  |
| `is_deleted` | boolean |  |
| `last_modified_at` | date |  |
| `name` | string |  |
| `nickname` | string |  |
| `source` | string |  |
| `status` | string |  |
| `tags` | array<number> |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /ca/api/account/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-bank-account.md) for the provider-specific parameters and requirements.

