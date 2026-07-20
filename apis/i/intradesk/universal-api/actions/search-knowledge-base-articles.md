# Intradesk: Search Knowledge Base Articles

Finds knowledge base articles in Intradesk by search text.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-knowledge-base-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-knowledge-base-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-knowledge-base-articles?${params}`, {
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
| `searchString` | string | no | Knowledge base hint search text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of knowledge base hint results to skip. Defaults to 0. |
| `take` | number | no | Maximum number of knowledge base hint results to return. Defaults to 10. |
| `servicePath` | string | no | Optional service path filter for knowledge base hints. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /knowledgebase/api/v1/Hints/search` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-knowledge-base-articles.md) for the provider-specific parameters and requirements.

