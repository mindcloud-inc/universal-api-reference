# Happy SMS: List Documents



```
GET https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/list-documents?${params}`, {
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
| `page` | number | no | Zero-based page number. |
| `limit` | number | no | Maximum number of documents to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Sort expression such as key;ASC. |
| `queryFilter` | string | no | RSQL filter expression for narrowing documents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data[]": [
        {
          "key": "string",
          "label": "string",
          "type": "string",
          "value": "string"
        }
      ],
      "listInfoMessages": [
        [
          "string"
        ]
      ],
      "listWarningMessages": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Total number of matching documents. |
| `data[][].key` | string | Generated property key. |
| `data[][].label` | string | Document property label. |
| `data[][].type` | string | Document property type. |
| `data[][].value` | string | Document property value. |
| `listInfoMessages[]` | array<string> | Informational messages returned by the API. |
| `listWarningMessages[]` | array<string> | Warning messages returned by the API. |

## Native endpoint

Through the native Happy SMS API, this operation is `GET /api/v1/protected/domain/custom-data/documents` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

