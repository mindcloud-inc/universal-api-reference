# Natif.ai: Get Document PDF

Retrieves a processed document PDF from Natif.ai.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-document-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-document-pdf?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-document-pdf?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Natif.ai API returns.

## Native endpoint

Through the native Natif.ai API, this operation is `GET /documents/[:documentId]/pdf` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-pdf.md) for the provider-specific parameters and requirements.

