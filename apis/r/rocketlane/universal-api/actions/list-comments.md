# Rocketlane: List Comments

Lists comments in Rocketlane.

```
GET https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-comments?${params}`, {
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
| `sourceType` | string | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `match` | string | no | You can use the match param to specify if we need to filter the entries using either AND(all) / OR(any). Defaults to AND. |
| `includeFields` | list<string> | no | Use this query parameter to opt in for fields to be returned in the response body. Use comma separated values to fetch the respective fields. If left blank, default properties are returned. |

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

Through the native Rocketlane API, this operation is `GET /1.0/comments` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

