# ME-QR: List QRs

Retrieves all QR codes from ME-QR.

```
GET https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/list-q-rs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ME-QR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/list-q-rs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/list-q-rs?${params}`, {
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
| `page` | number | no | Set page number. |
| `limit` | number | no | Set limit of qrs per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPageNumber": 1,
      "items": [
        {}
      ],
      "lastPageNumber": 1,
      "numItemsPerPage": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPageNumber` | number |  |
| `items` | array<object> |  |
| `lastPageNumber` | number |  |
| `numItemsPerPage` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ME-QR API, this operation is `GET /api/qr/list/` (base URL `https://me-qr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-q-rs.md) for the provider-specific parameters and requirements.

