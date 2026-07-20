# Rocketlane: Create Comment

Creates a comment in Rocketlane.

```
POST https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "source": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "source": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeFields` | string | no |  |
| `content` | string | yes | Content of the comment |
| `source` | object | yes | Source associated with the comment |
| `attachments` | list<object> | no | List of attachments associated with the comment |
| `private` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "commentId": 1,
      "content": "string",
      "createdAt": 1,
      "createdBy": {},
      "private": true,
      "source": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | List of attachments associated with the comment |
| `commentId` | number | Unique identifier for the comment |
| `content` | string | Content of the comment |
| `createdAt` | number | Timestamp representing the creation time of the comment |
| `createdBy` | object | Details of the user who created the comment |
| `private` | boolean | Indicates whether the comment is private or public |
| `source` | object | Source associated with the comment |

## Native endpoint

Through the native Rocketlane API, this operation is `POST /1.0/comments` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

