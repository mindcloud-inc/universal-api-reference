# Canny: Merge Idea

Merges an idea into another idea in Canny.

```
PUT https://connect.mindcloud.co/v1/universal/canny/latest/actions/merge-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/canny/latest/actions/merge-idea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mergeIdeaID": "string",
  "intoIdeaID": "string",
  "mergerID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canny/latest/actions/merge-idea', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mergeIdeaID": "string",
    "intoIdeaID": "string",
    "mergerID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mergeIdeaID` | string | yes | The idea unique identifier that will be merged. |
| `intoIdeaID` | string | yes | The idea unique identifier that the merge idea will be merged into. |
| `mergerID` | string | yes | The unique identifier of the user performing the merge. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native Canny API, this operation is `POST /v1/ideas/merge` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-idea.md) for the provider-specific parameters and requirements.

