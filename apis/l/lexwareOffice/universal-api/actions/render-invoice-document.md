# Lexware Office: Render Invoice Document

Retrieves a rendered invoice PDF from Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/render-invoice-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/render-invoice-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/render-invoice-document?${params}`, {
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
| `id` | string | yes | The Lexware invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentFileId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentFileId` | string |  |

## Native endpoint

Through the native Lexware Office API, this operation is `GET /v1/invoices/:id/document` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-invoice-document.md) for the provider-specific parameters and requirements.

