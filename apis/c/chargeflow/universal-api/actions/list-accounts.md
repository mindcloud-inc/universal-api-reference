# Chargeflow: List Accounts

Retrieves Chargeflow Connect accounts from your workspace.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-accounts?${params}`, {
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
| `limit` | number | no | Maximum number of records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "ext_account_id": "string",
          "id": "string",
          "owner_name": "Ava Chen"
        }
      ],
      "pagination": {
        "totalCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> |  |
| `accounts[].created_at` | date |  |
| `accounts[].ext_account_id` | string |  |
| `accounts[].id` | string |  |
| `accounts[].owner_name` | string |  |
| `pagination.totalCount` | number |  |

## Native endpoint

Through the native Chargeflow API, this operation is `GET /accounts` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

