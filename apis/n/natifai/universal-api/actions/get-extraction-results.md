# Natif.ai: Get Extraction Results

Retrieves extraction results for a document from Natif.ai.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-extraction-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-extraction-results?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-extraction-results?${params}`, {
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
| `documentId` | string | yes | UUID of the document. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaVersion` | number | no | Extraction schema version. Pass `-1` for the latest schema. Default: `-1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Natif.ai API returns.

## Native endpoint

Through the native Natif.ai API, this operation is `GET /documents/[:documentId]/extractions` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extraction-results.md) for the provider-specific parameters and requirements.

