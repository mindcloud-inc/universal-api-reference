# Longreads: Get Coauthor

Retrieves a Longreads coauthor by nicename.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-coauthor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-coauthor?connectionId=$CONNECTION_ID&userNicename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userNicename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-coauthor?${params}`, {
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
| `userNicename` | string | yes | The coauthor nicename slug to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": {},
      "display_name": "Ava Chen",
      "id": 1,
      "link": "https://example.com",
      "slug": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | object |  |
| `display_name` | string |  |
| `id` | number |  |
| `link` | string |  |
| `slug` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /coauthors/v1/coauthors/{user_nicename}` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coauthor.md) for the provider-specific parameters and requirements.

