# Affinda: Get list of all annotations

Retrieves annotations for an Affinda document.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-annotations?connectionId=$CONNECTION_ID&document=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-annotations?${params}`, {
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
| `document` | string | yes | Filter by document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classificationConfidence": 1,
      "confidence": 1,
      "contentType": "string",
      "dataPoint": "string",
      "document": "string",
      "field": "string",
      "id": 1,
      "isAutoVerified": true,
      "isClientVerified": true,
      "isVerified": true,
      "pageIndex": 1,
      "parent": 1,
      "raw": "string",
      "rectangle": {},
      "rectangles": [
        {}
      ],
      "textExtractionConfidence": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classificationConfidence` | number |  |
| `confidence` | number |  |
| `contentType` | string |  |
| `dataPoint` | string |  |
| `document` | string |  |
| `field` | string |  |
| `id` | number |  |
| `isAutoVerified` | boolean |  |
| `isClientVerified` | boolean |  |
| `isVerified` | boolean |  |
| `pageIndex` | number |  |
| `parent` | number |  |
| `raw` | string |  |
| `rectangle` | object |  |
| `rectangles` | array<object> |  |
| `textExtractionConfidence` | number |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/annotations` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-annotations.md) for the provider-specific parameters and requirements.

