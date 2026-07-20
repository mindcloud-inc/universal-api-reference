# Column: Create Bank Account



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/create-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/create-bank-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "entityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/create-bank-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "entityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes |  |
| `entityId` | string | yes |  |
| `displayName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isInterestBearing` | boolean | no |  |
| `interestConfigId` | string | no |  |
| `isOverdraftable` | boolean | no |  |
| `overdraftReserveAccountId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `POST /bank-accounts` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bank-account.md) for the provider-specific parameters and requirements.

