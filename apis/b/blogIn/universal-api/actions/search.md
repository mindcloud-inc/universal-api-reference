# BlogIn: Search

Finds matching content in BlogIn by search terms.

```
GET https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/search?connectionId=$CONNECTION_ID&terms=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "terms": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/search?${params}`, {
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
| `terms` | string | yes | The search terms to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "date_published": "string",
      "id": 1,
      "resourceType": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `date_published` | string |  |
| `id` | number |  |
| `resourceType` | string |  |
| `title` | string |  |

## Native endpoint

Through the native BlogIn API, this operation is `GET /search` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

