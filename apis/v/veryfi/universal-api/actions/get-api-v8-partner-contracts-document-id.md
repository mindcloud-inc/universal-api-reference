# Veryfi: Get a Contract

Retrieves a contract from Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-contracts-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-contracts-document-id?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-contracts-document-id?${params}`, {
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
| `documentId` | string | yes |  |
| `boundingBoxes` | boolean | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidenceDetails` | boolean | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veryfi API returns.

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/contracts/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-contracts-document-id.md) for the provider-specific parameters and requirements.

