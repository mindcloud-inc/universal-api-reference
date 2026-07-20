# Kintone: List Comments

Retrieves comments from a Kintone record.

```
GET https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-comments?connectionId=$CONNECTION_ID&appId=1&recordId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1",
  "recordId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-comments?${params}`, {
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
| `appId` | number | yes | The Kintone app ID. |
| `recordId` | number | yes | The Kintone record ID. |
| `offset` | number | no | Number of comments to skip before returning results. |
| `limit` | number | no | Maximum number of comments to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | string | no | Comment sort order. Use asc for oldest first or desc for newest first. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "newer": true,
      "older": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> | The record comments returned by Kintone. |
| `newer` | boolean | Whether newer comments remain available beyond this page. |
| `older` | boolean | Whether older comments remain available beyond this page. |

## Native endpoint

Through the native Kintone API, this operation is `GET /record/comments.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

