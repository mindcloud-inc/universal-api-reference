# arXiv: Get Paper By ID

Retrieves a paper from arXiv by ID.

```
GET https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/get-paper-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a arXiv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/get-paper-by-id?connectionId=$CONNECTION_ID&idList=2501.01234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idList": "2501.01234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/get-paper-by-id?${params}`, {
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
| `idList` | string | yes | Required single arXiv paper ID, for example 2501.01234 or cs/9901001. Example: `2501.01234`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arxiv:comment": "string",
      "arxiv:primary_category": {},
      "author": [
        {}
      ],
      "category": [
        {}
      ],
      "id": "string",
      "published": "2026-05-07T12:00:00.000Z",
      "summary": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arxiv:comment` | string | Optional arXiv comment field. |
| `arxiv:primary_category` | object | Primary arXiv category object. |
| `author` | array<object> | Author list objects containing author names. |
| `category` | array<object> | Category list objects from the Atom feed. |
| `id` | string | Canonical arXiv abstract URL for the paper version. |
| `published` | date | Original submission timestamp for version 1. |
| `summary` | string | Paper abstract. |
| `title` | string | Paper title. |
| `updated` | date | Last update timestamp for this paper version. |

## Native endpoint

Through the native arXiv API, this operation is `GET /query` (base URL `https://export.arxiv.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-paper-by-id.md) for the provider-specific parameters and requirements.

