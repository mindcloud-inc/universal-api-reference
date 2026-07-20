# Scoro: View Finance Account

Retrieves finance account details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-finance-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-finance-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-finance-account?${params}`, {
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
| `id` | string | no | Scoro finance account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "account_symbol": "string",
      "is_active": 1,
      "name": "Ava Chen",
      "parent_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `account_symbol` | string |  |
| `is_active` | number |  |
| `name` | string |  |
| `parent_id` | number |  |

## Native endpoint

Through the native Scoro API, this operation is `POST financeAccounts/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-finance-account.md) for the provider-specific parameters and requirements.

