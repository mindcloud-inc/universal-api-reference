# Startquestion: Append Respondent Batch

Adds respondents to a Startquestion batch.

```
POST https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/append-respondent-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/append-respondent-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/append-respondent-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchId` | string | yes | Batch ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "patch_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `patch_id` | string | Created respondent patch ID. |

## Native endpoint

Through the native Startquestion API, this operation is `POST /respondents/patch` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/append-respondent-batch.md) for the provider-specific parameters and requirements.

