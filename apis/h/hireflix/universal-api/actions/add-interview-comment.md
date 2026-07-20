# Hireflix: Add Interview Comment

Creates an interview comment in Hireflix.

```
POST https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/add-interview-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/add-interview-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string",
  "variables.comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/add-interview-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string",
    "variables.comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.id` | string | yes | The Hireflix interview ID. |
| `variables.comment` | string | yes | The comment to add to the interview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {
          "createdAt": 1,
          "id": "string",
          "updatedAt": 1,
          "value": "string"
        }
      ],
      "id": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments[].createdAt` | number |  |
| `comments[].id` | string |  |
| `comments[].updatedAt` | number |  |
| `comments[].value` | string |  |
| `id` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-interview-comment.md) for the provider-specific parameters and requirements.

