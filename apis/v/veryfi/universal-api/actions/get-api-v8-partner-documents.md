# Veryfi: Search Documents

Finds documents in Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents?${params}`, {
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
| `page` | number | no | Default value: 1 The page number. The response is capped to maximum of 50 results per page. |
| `pageSize` | number | no | Default value: 50 The number of Documents per page. |
| `boundingBoxes` | boolean | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidenceDetails` | boolean | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
| `detailed` | boolean | no | This field was deprecated on 2023-08-20. Use bounding_boxes and confidence_details . |
| `q` | string | no | Case sensitive. Return documents with this text or any extracted fields matching the value exactly. Also matches external_id , notes . Use asterisk for partial matches, e.g. q=Walmart* will return documents with either Walmart in ocr text, any extracted field containing Walmart, or external_id or notes containing Walmart. |
| `orderBy` | string | no | Default value: -created A field used to determine how to order the Documents in the response. For example, the value -created orders by created date with the most recent processed document at the top of the response. |
| `externalId` | string | no | A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `deviceId` | string | no |  |
| `deviceUserUuid` | string | no |  |
| `status` | string | no | The value indicating the document's status. |
| `tag` | string | no | An identifier used to help categorize or flag particular types of documents. Use this field to only return Documents with a specific tag. The Document object can have multiple tags. You can create tags by API or in Hub . |
| `owner` | string | no | The API username for the account that processed the document. |
| `createdGt` | string | no | Return documents created after this date and time in UTC ISO 8601 format . |
| `createdLt` | string | no | Return documents created before this date and time in UTC ISO 8601 format . |
| `createdGte` | string | no | Return documents created beginning at this date and time in UTC ISO 8601 format . |
| `createdLte` | string | no | Return documents created on and before this date and time in UTC ISO 8601 format . |
| `updatedGt` | string | no | Return documents updated after this date and time in UTC ISO 8601 format . |
| `updatedLt` | string | no | Return documents updated before this date and time in UTC ISO 8601 format . |
| `updatedGte` | string | no | Return documents updated beginning at this date and time in UTC ISO 8601 format . |
| `updatedLte` | string | no | Return documents updated on and before this date and time in UTC ISO 8601 format . |
| `dateGt` | string | no | Return documents with the date field greater than this date and time in UTC ISO 8601 format . |
| `dateLt` | string | no | Return documents with the date field less than this date and time in UTC ISO 8601 format . |
| `dateGte` | string | no | Return documents with the date field greater than or equal to this date and time in UTC ISO 8601 format . |
| `dateLte` | string | no | Return documents with the date field less than or equal to this date and time in UTC ISO 8601 format . |
| `trackTotalResults` | boolean | no | Whether to always return accurate total_results and total_pages, true makes it slower. For increased performance, total results are not counted by default for search requests (with q parameter), and counted for list requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": [
        {}
      ],
      "error": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | array<object> |  |
| `error` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/documents` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-documents.md) for the provider-specific parameters and requirements.

