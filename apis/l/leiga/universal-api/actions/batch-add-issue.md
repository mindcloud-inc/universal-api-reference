# Leiga: Batch Add Issue

Creates multiple new issues in Leiga.

```
POST https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-add-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-add-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "issueTypeId": 1,
  "datas[]": [
    {}
  ],
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-add-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "issueTypeId": 1,
    "datas[]": [{}],
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
| `datas[]` | array<object> | yes | Issues Field Values |
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failureReason": "string",
      "issueId": 1,
      "success": true,
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failureReason` | string | Failure reason when create fails. |
| `issueId` | number | Created issue ID. |
| `success` | boolean | Whether the issue create succeeded. |
| `summary` | string | Issue summary. |

## Native endpoint

Through the native Leiga API, this operation is `POST /issue/batch-add` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-add-issue.md) for the provider-specific parameters and requirements.

