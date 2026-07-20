# Ortto: Upsert Accounts



```
POST https://connect.mindcloud.co/v1/universal/ortto/latest/actions/upsert-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/upsert-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accounts[]": [
    {}
  ],
  "merge_by[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/upsert-accounts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accounts[]": [{}],
    "merge_by[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accounts[]` | array<object> | yes | Accounts to create or update. |
| `merge_by[]` | array<string> | yes | Account fields used to find existing accounts. |
| `async` | boolean | no | Queue the merge asynchronously. |
| `mergeStrategy` | number | no | How existing account values should be merged. |
| `findStrategy` | number | no | How merge fields should be used when finding accounts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {
          "accountId": "string",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts[].accountId` | string |  |
| `accounts[].status` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /accounts/merge` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-accounts.md) for the provider-specific parameters and requirements.

