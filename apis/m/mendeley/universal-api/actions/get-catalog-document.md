# Mendeley: Get Catalog Document



```
GET https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-catalog-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-catalog-document?connectionId=$CONNECTION_ID&id=eaede082-7d8b-3f0c-be3a-fb7be685fbe6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "eaede082-7d8b-3f0c-be3a-fb7be685fbe6"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-catalog-document?${params}`, {
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
| `id` | string | yes | The catalog id (UUID). Example: `eaede082-7d8b-3f0c-be3a-fb7be685fbe6`. |
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
      "groupCount": 1,
      "hasPdf": true,
      "id": "string",
      "identifiers": {},
      "link": "https://example.com",
      "readerCount": 1,
      "readerCountByAcademicStatus": {},
      "readerCountByCountry": {},
      "readerCountBySubdiscipline": {},
      "readerCountBySubjectArea": {},
      "readerCountByUserRole": {},
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
| `groupCount` | number |  |
| `hasPdf` | boolean |  |
| `id` | string |  |
| `identifiers` | object |  |
| `link` | string |  |
| `readerCount` | number |  |
| `readerCountByAcademicStatus` | object |  |
| `readerCountByCountry` | object |  |
| `readerCountBySubdiscipline` | object |  |
| `readerCountBySubjectArea` | object |  |
| `readerCountByUserRole` | object |  |
| `source` | string |  |
| `title` | string |  |
| `type` | string |  |
| `year` | number |  |

## Native endpoint

Through the native Mendeley API, this operation is `GET /catalog/:id` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-document.md) for the provider-specific parameters and requirements.

