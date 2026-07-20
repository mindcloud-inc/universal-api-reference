# Leiga: Batch Add Subtasks

Creates multiple new subtasks in Leiga.

```
POST https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-add-subtasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-add-subtasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "issueId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leiga/latest/actions/batch-add-subtasks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "issueId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issueId` | number | yes | Parent Issue ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issueAddVOList": [
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
| `issueAddVOList` | array<object> | Created subtask results. |

## Native endpoint

Through the native Leiga API, this operation is `POST /issue/batch-add-subtask` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-add-subtasks.md) for the provider-specific parameters and requirements.

