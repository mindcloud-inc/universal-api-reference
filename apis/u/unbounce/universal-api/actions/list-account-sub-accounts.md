# Unbounce: List Account Sub Accounts

Retrieves sub-accounts for a specified Unbounce account.

```
GET https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-account-sub-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-account-sub-accounts?connectionId=$CONNECTION_ID&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-account-sub-accounts?${params}`, {
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
| `account_id` | string | yes | Unbounce account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "subAccounts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object |  |
| `subAccounts` | array<object> |  |

## Native endpoint

Through the native Unbounce API, this operation is `GET /accounts/:account_id/sub_accounts` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-sub-accounts.md) for the provider-specific parameters and requirements.

