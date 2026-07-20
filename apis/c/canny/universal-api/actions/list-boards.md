# Canny: List Boards

Retrieves all available boards from Canny.

```
GET https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-boards?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isPrivate": true,
      "name": "Ava Chen",
      "postCount": 1,
      "privateComments": true,
      "token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `name` | string |  |
| `postCount` | number |  |
| `privateComments` | boolean |  |
| `token` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Canny API, this operation is `POST /v1/boards/list` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-boards.md) for the provider-specific parameters and requirements.

