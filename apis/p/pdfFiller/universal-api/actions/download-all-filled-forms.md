# PdfFiller: Download All Filled Forms

Downloads all filled forms from a PdfFiller fill request.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/download-all-filled-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/download-all-filled-forms?connectionId=$CONNECTION_ID&linkToFillId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkToFillId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/download-all-filled-forms?${params}`, {
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
| `linkToFillId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PdfFiller API returns.

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/fillable_forms/:linkToFillId/download` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-all-filled-forms.md) for the provider-specific parameters and requirements.

