# Ortto: Delete Accounts



```
DELETE https://connect.mindcloud.co/v1/universal/ortto/latest/actions/delete-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/delete-accounts?connectionId=$CONNECTION_ID&inclusion_ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inclusion_ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/delete-accounts?${params}`, {
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
| `inclusion_ids[]` | array<string> | yes | Account IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedAccounts": 1,
      "scheduledAccounts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedAccounts` | number |  |
| `scheduledAccounts` | number |  |

## Native endpoint

Through the native Ortto API, this operation is `DELETE /accounts/delete` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-accounts.md) for the provider-specific parameters and requirements.

