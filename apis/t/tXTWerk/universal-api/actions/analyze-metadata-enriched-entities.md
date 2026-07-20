# TXT Werk: Analyze Metadata-Enriched Entities

Retrieves metadata-enriched entities from text in TXT Werk.

```
GET https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-metadata-enriched-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TXT Werk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-metadata-enriched-entities?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-metadata-enriched-entities?${params}`, {
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
| `text` | string | yes |  |
| `language` | string | no |  |
| `nentities` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "language": "string",
      "text": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `language` | string |  |
| `text` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native TXT Werk API, this operation is `POST /rest/txt/analyzer` (base URL `https://api.txtwerk.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-metadata-enriched-entities.md) for the provider-specific parameters and requirements.

