# Docparser: Get Sorted Data Of Multiple Documents

Retrieves sorted parsed data for multiple Docparser documents.

```
GET https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-sorted-data-of-multiple-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-sorted-data-of-multiple-documents?connectionId=$CONNECTION_ID&parserId=tiumtyrcddpn&sortBy=uploaded_at" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parserId": "tiumtyrcddpn",
  "sortBy": "uploaded_at"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-sorted-data-of-multiple-documents?${params}`, {
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
| `parserId` | string | yes | Use the parser ID returned by List Document Parsers. Example: `tiumtyrcddpn`. |
| `sortBy` | string | yes | Choose the field Docparser should sort by. Example: `uploaded_at`. |
| `sortOrder` | string | no | Choose whether Docparser sorts ascending or descending. One of: `0`, `1`. Example: `desc`. |
| `limit` | number | no | Maximum number of parsed documents to return. Example: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeProcessingQueue` | boolean | no | Include documents that are still waiting in the processing queue. Example: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docparser API returns.

## Native endpoint

Through the native Docparser API, this operation is `GET /v1/results/:PARSER_ID` (base URL `https://api.docparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sorted-data-of-multiple-documents.md) for the provider-specific parameters and requirements.

