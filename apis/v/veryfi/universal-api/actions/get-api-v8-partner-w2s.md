# Veryfi: Get W-2s

Retrieves W-2 documents from Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-w2s
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-w2s?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-w2s?${params}`, {
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
| `metaTags[]` | array<string> | no | Return documents containing these tags. |
| `metaExternalId` | string | no | Return documents with this meta.external_id. |
| `createdDateGt` | string | no | Return documents created after this date and time in ISO 8601 format . |
| `createdDateLt` | string | no | Return documents created before this date and time in ISO 8601 format . |
| `createdDateGte` | string | no | Return documents created beginning at this date and time in ISO 8601 format . |
| `createdDateLte` | string | no | Return documents created on and before this date and time in ISO 8601 format . |
| `updatedDateGt` | string | no | Return documents updated after this date and time in ISO 8601 format . |
| `updatedDateLt` | string | no | Return documents updated before this date and time in ISO 8601 format . |
| `updatedDateGte` | string | no | Return documents updated beginning at this date and time in ISO 8601 format . |
| `updatedDateLte` | string | no | Return documents updated on and before this date and time in ISO 8601 format . |
| `page` | number | no | Default value: 1 The page number. The response is capped to maximum of 50 results per page. |
| `pageSize` | number | no | Default value: 50 The number of Documents per page. |
| `boundingBoxes` | boolean | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidenceDetails` | boolean | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
| `q` | string | no | Case sensitive. Return documents with this text or any extracted fields matching the value. Use asterisk for partial matches, e.g. q=Walmart* will return documents with either Walmart in ocr text or any extracted field containing Walmart. |
| `trackTotalResults` | boolean | no | Whether to always return accurate count of results, true makes it slower. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veryfi API returns.

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/w2s` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-w2s.md) for the provider-specific parameters and requirements.

