# Geral: List QR Codes

Retrieves QR codes from Geral.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-qr-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-qr-codes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-qr-codes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "datetime": "2026-05-07T12:00:00.000Z",
      "embedded_data": "string",
      "id": 1,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "qr_code": "https://example.com",
      "qr_code_background": "https://example.com",
      "qr_code_logo": "https://example.com",
      "settings": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date | Creation timestamp. |
| `embedded_data` | string | Data embedded in the QR code. |
| `id` | number | QR code ID. |
| `last_datetime` | date | Last update timestamp. |
| `name` | string | QR code name. |
| `qr_code` | string | QR code image URL. |
| `qr_code_background` | string | QR code background URL. |
| `qr_code_logo` | string | QR code logo URL. |
| `settings` | object | QR code settings. |
| `type` | string | QR code type. |

## Native endpoint

Through the native Geral API, this operation is `GET /qr-codes/` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-qr-codes.md) for the provider-specific parameters and requirements.

