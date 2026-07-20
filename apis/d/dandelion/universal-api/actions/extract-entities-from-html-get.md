# Dandelion: Extract Entities From HTML via HTTP GET

Retrieves entities from HTML in Dandelion via HTTP GET.

```
GET https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/extract-entities-from-html-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dandelion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/extract-entities-from-html-get?connectionId=$CONNECTION_ID&html=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "html": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/extract-entities-from-html-get?${params}`, {
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
| `html` | string | yes | HTML to analyze. |
| `lang` | string | no | ISO 639-1 language code or auto. |
| `topEntities` | number | no | Number of top-ranked entities to include. |
| `minConfidence` | number | no | Discard entities below this confidence threshold. |
| `minLength` | number | no | Discard entities with spots shorter than this length. |
| `social.hashtag` | boolean | no | Parse hashtags as entities. |
| `social.mention` | boolean | no | Parse social mentions as entities. |
| `include` | string | no | Comma-separated list of extra fields to include. |
| `extraTypes` | string | no | Comma-separated list of extra type providers. |
| `country` | string | no | Country code used for better disambiguation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        {}
      ],
      "lang": "string",
      "langConfidence": 1,
      "text": "string",
      "time": 1,
      "timestamp": "string",
      "topEntities": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations` | array<object> |  |
| `lang` | string |  |
| `langConfidence` | number |  |
| `text` | string |  |
| `time` | number |  |
| `timestamp` | string |  |
| `topEntities` | array<object> |  |

## Native endpoint

Through the native Dandelion API, this operation is `GET /datatxt/nex/v1` (base URL `https://api.dandelion.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-entities-from-html-get.md) for the provider-specific parameters and requirements.

