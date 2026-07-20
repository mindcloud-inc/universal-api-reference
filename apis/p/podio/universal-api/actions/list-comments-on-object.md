# Podio: List Comments on Object

Retrieves comments on a Podio object.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-comments-on-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-comments-on-object?connectionId=$CONNECTION_ID&limit=25&offset=0&type=item&id=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "type": "item",
  "id": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-comments-on-object?${params}`, {
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
| `type` | string | yes | The type of object to read comments from. Example: `item`. |
| `id` | string | yes | The ID of the object to read comments from. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": 1,
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "embed": {},
      "embedFile": {},
      "externalId": "string",
      "files": [
        {}
      ],
      "grantedUsers": [
        {}
      ],
      "invitedUsers": [
        {}
      ],
      "isLiked": true,
      "lastEditOn": "2026-05-07T12:00:00.000Z",
      "likeCount": 1,
      "questions": [
        {}
      ],
      "ref": {},
      "richValue": "string",
      "rights": [
        "string"
      ],
      "user": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | number |  |
| `createdBy` | object |  |
| `createdOn` | date |  |
| `createdVia` | object |  |
| `embed` | object |  |
| `embedFile` | object |  |
| `externalId` | string |  |
| `files` | array<object> |  |
| `grantedUsers` | array<object> |  |
| `invitedUsers` | array<object> |  |
| `isLiked` | boolean |  |
| `lastEditOn` | date |  |
| `likeCount` | number |  |
| `questions` | array<object> |  |
| `ref` | object |  |
| `richValue` | string |  |
| `rights` | array<string> |  |
| `user` | object |  |
| `value` | string |  |

## Native endpoint

Through the native Podio API, this operation is `GET /comment/:type/:id/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments-on-object.md) for the provider-specific parameters and requirements.

