# Fintoc: List Accounts

Retrieves accounts from Fintoc.

```
GET https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-accounts?${params}`, {
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
      "available_balance": 1,
      "currency": "string",
      "description": "string",
      "entity": {},
      "id": "string",
      "is_root": true,
      "mode": "string",
      "object": "string",
      "root_account_number": "string",
      "root_account_number_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_balance` | number |  |
| `currency` | string |  |
| `description` | string |  |
| `entity` | object |  |
| `id` | string |  |
| `is_root` | boolean |  |
| `mode` | string |  |
| `object` | string |  |
| `root_account_number` | string |  |
| `root_account_number_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `GET /v2/accounts` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

