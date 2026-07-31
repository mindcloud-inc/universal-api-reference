# PoetryDB: Get Poems by Title



```
GET https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PoetryDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-title?connectionId=$CONNECTION_ID&title=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "title": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-title?${params}`, {
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
| `title` | string | yes | Required poem title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "linecount": "string",
      "lines": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `linecount` | string |  |
| `lines` | array<string> |  |
| `title` | string |  |

## Native endpoint

Through the native PoetryDB API, this operation is `GET /title/:title` (base URL `https://poetrydb.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-poems-by-title.md) for the provider-specific parameters and requirements.

