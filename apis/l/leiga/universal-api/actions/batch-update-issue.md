# Leiga: Batch Update Issue

Updates multiple existing issues in Leiga.

```
PUT https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-update-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-update-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "issueTypeId": 1,
  "data": {},
  "issueIds[]": [
    1
  ],
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-update-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "issueTypeId": 1,
    "data": {},
    "issueIds[]": [1],
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issueTypeId` | number | yes | Issue Type ID |
| `data` | object | yes | Issues Field Values |
| `issueIds[]` | array<number> | yes | Issue IDs |
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failureReason": "string",
      "issueId": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failureReason` | string | Failure reason when update fails. |
| `issueId` | number | Updated issue ID. |
| `success` | boolean | Whether the issue update succeeded. |

## Native endpoint

Through the native Leiga API, this operation is `PATCH /issue/batch-update` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-issue.md) for the provider-specific parameters and requirements.

