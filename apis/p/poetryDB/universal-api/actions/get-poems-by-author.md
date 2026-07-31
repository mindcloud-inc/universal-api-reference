# PoetryDB: Get Poems by Author



```
GET https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-author
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PoetryDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-author?connectionId=$CONNECTION_ID&author=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "author": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-author?${params}`, {
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
| `author` | string | yes | Required author name. |

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

Through the native PoetryDB API, this operation is `GET /author/:author` (base URL `https://poetrydb.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-poems-by-author.md) for the provider-specific parameters and requirements.

