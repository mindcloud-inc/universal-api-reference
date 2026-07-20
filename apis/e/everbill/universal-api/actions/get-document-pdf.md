# Everbill: Get Document PDF

Retrieves a document PDF from Everbill.

```
GET https://connect.mindcloud.co/v1/universal/everbill/latest/actions/get-document-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everbill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/get-document-pdf?connectionId=$CONNECTION_ID&document_name=Ava%20Chen&document_number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_name": "Ava Chen",
  "document_number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everbill/latest/actions/get-document-pdf?${params}`, {
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
| `document_name` | string | yes | Document type path segment, for example bills, offers, orders, or incoming_bills. |
| `document_number` | string | yes | Everbill document number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Everbill API returns.

## Native endpoint

Through the native Everbill API, this operation is `GET /:document_name/get_pdf/:document_number` (base URL `https://api.everbill.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-pdf.md) for the provider-specific parameters and requirements.

