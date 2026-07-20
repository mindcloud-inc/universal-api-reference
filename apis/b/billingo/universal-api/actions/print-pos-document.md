# Billingo: Print POS Document

Retrieves a printable POS document from Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/print-pos-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/print-pos-document?connectionId=$CONNECTION_ID&id=0&size=80" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0",
  "size": "80"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/print-pos-document?${params}`, {
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
| `id` | number | yes | Billingo document ID from the path. Default: `0`. |
| `size` | string | yes | POS print paper size required by Billingo. Default: `80`. Example: `80`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /documents/:id/print/pos` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/print-pos-document.md) for the provider-specific parameters and requirements.

