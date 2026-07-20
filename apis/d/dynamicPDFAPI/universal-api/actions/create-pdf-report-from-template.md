# DynamicPDF: Create PDF Report From Template

Creates a PDF report from a template in DynamicPDF API.

```
POST https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/create-pdf-report-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynamicPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/create-pdf-report-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "DlexPath": "string",
  "LayoutData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/create-pdf-report-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "DlexPath": "string",
    "LayoutData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `DlexPath` | string | yes | Cloud storage path to the DLEX template. |
| `LayoutData` | file | yes | JSON layout data file for the DLEX template. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynamicPDF API returns.

## Native endpoint

Through the native DynamicPDF API, this operation is `POST /v1.0/dlex-layout` (base URL `https://api.dpdf.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-report-from-template.md) for the provider-specific parameters and requirements.

