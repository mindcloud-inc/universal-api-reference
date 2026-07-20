# Sign.Plus: List Envelope Documents



```
GET https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelope-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelope-documents?connectionId=$CONNECTION_ID&envelopeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelopeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelope-documents?${params}`, {
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
| `envelopeId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {
          "filename": "Ava Chen",
          "id": "string",
          "name": "Ava Chen",
          "page_count": 1,
          "pages": [
            {
              "height": 1,
              "width": 1
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> |  |
| `documents[].filename` | string |  |
| `documents[].id` | string |  |
| `documents[].name` | string |  |
| `documents[].page_count` | number |  |
| `documents[].pages` | array<object> |  |
| `documents[].pages[].height` | number |  |
| `documents[].pages[].width` | number |  |

## Native endpoint

Through the native Sign.Plus API, this operation is `GET /envelope/:envelope_id/documents` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-envelope-documents.md) for the provider-specific parameters and requirements.

