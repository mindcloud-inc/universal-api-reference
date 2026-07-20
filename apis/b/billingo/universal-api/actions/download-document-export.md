# Billingo: Download Document Export

Retrieves an exported document file from Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/download-document-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/download-document-export?connectionId=$CONNECTION_ID&id=missing-export-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "missing-export-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/download-document-export?${params}`, {
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
| `id` | string | yes | Billingo document export ID from the path. Default: `missing-export-id`. |

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

Through the native Billingo API, this operation is `GET /document-export/:id/download` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-document-export.md) for the provider-specific parameters and requirements.

