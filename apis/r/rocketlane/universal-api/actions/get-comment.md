# Rocketlane: Get Comment

Retrieves a comment from Rocketlane.

```
GET https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-comment?connectionId=$CONNECTION_ID&commentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-comment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentId` | number | yes | The ID of the comment object |
| `includeFields` | list<string> | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |

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

Through the native Rocketlane API, this operation is `GET /1.0/comments/:commentId` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

