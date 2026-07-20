# Sisense: Create Extract Security Rules In Bulk

Creates extract security rules in Sisense.

```
POST https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-extract-security-rules-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-extract-security-rules-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "[0].server": "string",
  "[0].elasticube": "string",
  "[0].table": "string",
  "[0].column": "string",
  "[0].datatype": "text",
  "[0].allMembers": "true",
  "[0].shares[0].party": "string",
  "[0].shares[0].type": "user"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-extract-security-rules-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "[0].server": "string",
    "[0].elasticube": "string",
    "[0].table": "string",
    "[0].column": "string",
    "[0].datatype": "text",
    "[0].allMembers": "true",
    "[0].shares[0].party": "string",
    "[0].shares[0].type": "user"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `[0].server` | string | yes |  |
| `[0].elasticube` | string | yes |  |
| `[0].table` | string | yes |  |
| `[0].column` | string | yes |  |
| `[0].datatype` | string | yes | Default: `text`. |
| `[0].allMembers` | boolean | yes | Default: `true`. |
| `[0].shares[0].party` | string | yes |  |
| `[0].shares[0].type` | string | yes | Default: `user`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `POST /api/elasticubes/datasecurity` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-extract-security-rules-in-bulk.md) for the provider-specific parameters and requirements.

