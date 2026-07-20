# Uspacy: Create Comment

Creates a new comment in Uspacy.

```
POST https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityType": "string",
  "entityId": 1,
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityType": "string",
    "entityId": 1,
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | yes | The target entity type. |
| `entityId` | number | yes | The target entity ID. |
| `message` | string | yes | The comment message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": 1,
      "date": 1,
      "entityId": 1,
      "entityType": "string",
      "id": 1,
      "mentioned": [
        {}
      ],
      "message": "string",
      "notify": [
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
| `authorId` | number |  |
| `date` | number |  |
| `entityId` | number |  |
| `entityType` | string |  |
| `id` | number |  |
| `mentioned` | array<object> |  |
| `message` | string |  |
| `notify` | array<object> |  |

## Native endpoint

Through the native Uspacy API, this operation is `POST /comments/v1/comments` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

