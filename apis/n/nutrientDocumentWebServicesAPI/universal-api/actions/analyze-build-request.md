# Nutrient Document Web Services: Analyze Build Request

Analyzes a document build request in Nutrient Document Web Services API.

```
GET https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/analyze-build-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Web Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/analyze-build-request?connectionId=$CONNECTION_ID&parts%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parts[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/analyze-build-request?${params}`, {
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
| `parts[]` | array<object> | yes | Source document parts. |
| `actions[]` | array<object> | no | Build actions to apply. |
| `output` | object | no | Output configuration. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nutrient Document Web Services API returns.

## Native endpoint

Through the native Nutrient Document Web Services API, this operation is `POST /analyze_build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-build-request.md) for the provider-specific parameters and requirements.

