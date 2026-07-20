# PdfFiller: Delete Filled Form

Deletes an existing filled form from PdfFiller.

```
DELETE https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/delete-filled-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/delete-filled-form?connectionId=$CONNECTION_ID&linkToFillId=https%3A%2F%2Fexample.com&filledFormId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkToFillId": "https://example.com",
  "filledFormId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/delete-filled-form?${params}`, {
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
| `filledFormId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `total` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `DELETE /v2/fillable_forms/:linkToFillId/filled_forms/:filledFormId` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-filled-form.md) for the provider-specific parameters and requirements.

