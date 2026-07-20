# Dandelion: Compare HTML Fragment Similarity via HTTP POST

Retrieves HTML fragment similarity from Dandelion via HTTP POST.

```
GET https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/compare-html-fragment-similarity-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dandelion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/compare-html-fragment-similarity-post?connectionId=$CONNECTION_ID&htmlFragment1=string&htmlFragment2=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "htmlFragment1": "string",
  "htmlFragment2": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/compare-html-fragment-similarity-post?${params}`, {
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
| `htmlFragment1` | string | yes | First HTML fragment to compare. |
| `htmlFragment2` | string | yes | Second HTML fragment to compare. |
| `lang` | string | no | Language code or auto-detect. |
| `bow` | string | no | Fallback strategy: never, both_empty, one_empty, or always. |
| `nex.minConfidence` | number | no | Optional prefixed Entity Extraction parameter. |
| `nex.topEntities` | number | no | Optional prefixed Entity Extraction parameter. |
| `nex.include` | string | no | Optional prefixed Entity Extraction include values as a comma-separated list. |
| `nex.extraTypes` | string | no | Optional prefixed Entity Extraction extra types as a comma-separated list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lang": "string",
      "langConfidence": 1,
      "similarity": 1,
      "time": 1,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lang` | string |  |
| `langConfidence` | number |  |
| `similarity` | number |  |
| `time` | number |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Dandelion API, this operation is `POST /datatxt/sim/v1` (base URL `https://api.dandelion.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-html-fragment-similarity-post.md) for the provider-specific parameters and requirements.

