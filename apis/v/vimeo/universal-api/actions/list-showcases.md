# Vimeo: List Showcases

Retrieves a user's showcases from Vimeo.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-showcases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-showcases?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=152184" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "152184"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-showcases?${params}`, {
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
| `userId` | number | yes | The ID of the user. Example: `152184`. |
| `query` | string | no | The search query to use to filter the results. Example: `Stop motion`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | list<string> | no | The way to sort the results. One of: `alphabetical`, `date`, `duration`, `last_modified`, `videos`. Example: `date`. |
| `direction` | list<string> | no | The sort direction of the results. One of: `asc`, `desc`. Example: `asc`. |
| `filterPrivacy` | list<string> | no | A comma-separated list of showcase privacies to include. One of: `anybody`, `embed_only`, `nobody`, `password`, `team`, `unlisted`. Accepts multiple values in one string, delimited by `,`. Example: `anybody,password`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "layout": "string",
      "link": "https://example.com",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "shareLink": "https://example.com",
      "sort": "string",
      "theme": "string",
      "totalClips": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | When the showcase was created. |
| `description` | string | The showcase description. |
| `duration` | number | Total showcase duration in seconds. |
| `layout` | string | The showcase layout mode. |
| `link` | string | The public Vimeo showcase URL. |
| `modifiedTime` | date | When the showcase was last modified. |
| `name` | string | The showcase name. |
| `shareLink` | string | The share link for the showcase. |
| `sort` | string | The showcase sort mode. |
| `theme` | string | The showcase theme. |
| `totalClips` | number | Total number of clips in the showcase. |
| `uri` | string | The showcase API URI. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /users/:user_id/albums` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-showcases.md) for the provider-specific parameters and requirements.

