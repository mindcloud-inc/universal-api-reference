# Tettra: Create Question

Creates a new question in Tettra.

```
POST https://connect.mindcloud.co/v1/universal/tettra/latest/actions/create-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tettra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/create-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tettra/latest/actions/create-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignees` | list<number> | no | User IDs to assign the question to. |
| `categoryId` | number | no | Category to ask the question in. |
| `details` | string | no | Additional question details formatted as HTML. |
| `subcategoryId` | number | no | Subcategory to ask the question in. |
| `title` | string | yes | Question title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "questionUrl": "https://example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `questionUrl` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tettra API, this operation is `POST /teams/85329/questions` (base URL `https://app.tettra.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-question.md) for the provider-specific parameters and requirements.

