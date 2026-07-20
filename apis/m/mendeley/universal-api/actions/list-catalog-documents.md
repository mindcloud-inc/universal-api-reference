# Mendeley: List Catalog Documents



```
GET https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-catalog-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-catalog-documents?connectionId=$CONNECTION_ID&doi=10.1016%2Fj.molcel.2009.09.013" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "doi": "10.1016/j.molcel.2009.09.013"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-catalog-documents?${params}`, {
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
| `doi` | string | yes | Digital Object Identifier. Example: `10.1016/j.molcel.2009.09.013`. |
| `view` | string | no | Includes core document fields plus additional fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        {}
      ],
      "hasPdf": true,
      "id": "string",
      "identifiers": {},
      "link": "https://example.com",
      "source": "string",
      "title": "string",
      "type": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors` | array<object> |  |
| `hasPdf` | boolean |  |
| `id` | string |  |
| `identifiers` | object |  |
| `link` | string |  |
| `source` | string |  |
| `title` | string |  |
| `type` | string |  |
| `year` | number |  |

## Native endpoint

Through the native Mendeley API, this operation is `GET /catalog` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-catalog-documents.md) for the provider-specific parameters and requirements.

