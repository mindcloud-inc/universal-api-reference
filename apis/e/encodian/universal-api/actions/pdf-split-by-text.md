# Encodian: PDF Split By Text

Splits a PDF by text in Encodian.

```
DELETE https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-split-by-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-split-by-text?connectionId=$CONNECTION_ID&filename=Ava%20Chen&fileContent=string&splitValue=string&isExpression=true&prefixFilename=true&splitPdfByTextType=string&splitAction=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "Ava Chen",
  "fileContent": "string",
  "splitValue": "string",
  "isExpression": "true",
  "prefixFilename": "true",
  "splitPdfByTextType": "string",
  "splitAction": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-split-by-text?${params}`, {
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
| `filename` | string | yes | The filename of the source PDF document including the file extension. |
| `fileContent` | string | yes | A Base64 encoded representation of the source PDF document. |
| `splitValue` | string | yes | Specify either a text value or a regular expression. |
| `isExpression` | boolean | yes | Set whether to evaluate the split value as a string or regular expression. |
| `prefixFilename` | boolean | yes | Set whether the expression value should be used within the output filename. |
| `splitPdfByTextType` | string | yes | Select whether to split on the first instance, last instance, or all instances matching the split value. |
| `splitAction` | string | yes | Select whether to split on, before, after, or remove the page containing the split value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Documents": [
        {}
      ],
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Documents` | array<object> | The split PDF documents returned by the operation. |
| `Errors` | array<string> | Any error messages returned by the operation. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Indicates whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/SplitPdfByText` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-split-by-text.md) for the provider-specific parameters and requirements.

