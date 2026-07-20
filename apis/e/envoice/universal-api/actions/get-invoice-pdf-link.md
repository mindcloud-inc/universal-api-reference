# Envoice: Get Invoice PDF Link

Retrieves an invoice PDF URL from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-invoice-pdf-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-invoice-pdf-link?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-invoice-pdf-link?${params}`, {
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
| `id` | number | yes | Invoice identifier. |
| `signedVersion` | boolean | no | Whether to return the signed PDF version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Link` | string | Invoice PDF link. |

## Native endpoint

Through the native Envoice API, this operation is `GET invoice/pdf` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-pdf-link.md) for the provider-specific parameters and requirements.

