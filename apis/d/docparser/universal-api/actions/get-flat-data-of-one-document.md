# Docparser: Get Flat Data Of One Document

Retrieves flat parsed data for one Docparser document.

```
GET https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-flat-data-of-one-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-flat-data-of-one-document?connectionId=$CONNECTION_ID&parserId=tiumtyrcddpn&documentId=52d17ca7ac28434b11c5037127144251" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parserId": "tiumtyrcddpn",
  "documentId": "52d17ca7ac28434b11c5037127144251"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-flat-data-of-one-document?${params}`, {
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
| `documentId` | string | yes | Use the document ID returned by a parsed-data action. Example: `52d17ca7ac28434b11c5037127144251`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docparser API returns.

## Native endpoint

Through the native Docparser API, this operation is `GET /v1/results/:PARSER_ID/:DOCUMENT_ID` (base URL `https://api.docparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flat-data-of-one-document.md) for the provider-specific parameters and requirements.

