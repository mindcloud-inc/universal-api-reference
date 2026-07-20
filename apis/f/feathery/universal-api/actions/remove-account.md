# Feathery: Remove Account



```
DELETE https://connect.mindcloud.co/v1/universal/feathery/latest/actions/remove-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/remove-account?connectionId=$CONNECTION_ID&accounts%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accounts[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/remove-account?${params}`, {
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
| `accounts[]` | array<object> | yes | An array of account removal objects. Each object should include email or account_id per the Feathery docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "team": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> | The remaining accounts on the team after removal. |
| `team` | string | The name of your Feathery team. |

## Native endpoint

Through the native Feathery API, this operation is `PATCH /api/account/uninvite/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-account.md) for the provider-specific parameters and requirements.

