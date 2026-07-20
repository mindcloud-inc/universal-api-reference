# RotaCloud: List Accounts

Lists accounts in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-accounts?${params}`, {
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
      "billing_term": "string",
      "billing_type": "string",
      "created": "string",
      "expired": true,
      "features_disabled": [
        "string"
      ],
      "id": 1,
      "industry": 1,
      "level": "string",
      "name": "Ava Chen",
      "owner": 1,
      "permissions": [
        "string"
      ],
      "services": [
        {}
      ],
      "setup_steps": [
        {}
      ],
      "suspended": true,
      "timezone": 1,
      "total_employees": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_term` | string |  |
| `billing_type` | string |  |
| `created` | string |  |
| `expired` | boolean |  |
| `features_disabled` | array<string> |  |
| `id` | number |  |
| `industry` | number |  |
| `level` | string |  |
| `name` | string |  |
| `owner` | number |  |
| `permissions` | array<string> |  |
| `services` | array<object> |  |
| `setup_steps` | array<object> |  |
| `suspended` | boolean |  |
| `timezone` | number |  |
| `total_employees` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/accounts` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

