# BoothBook: List Bookings

Retrieves bookings from BoothBook.

```
GET https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoothBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/list-bookings?${params}`, {
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
| `start` | date | no | Start date in ISO format (YYYY-MM-DD). Example: `2026-03-27`. |
| `end` | date | no | End date in ISO format (YYYY-MM-DD). Example: `2026-03-28`. |
| `scope` | string | no | Use minimal or full to control booking response detail. Default: `minimal`. Example: `minimal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookings": {},
      "message": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookings` | object | Raw BoothBook booking map keyed by booking ID until runtime mapper verification is completed. |
| `message` | string |  |
| `result` | string | BoothBook result status. |

## Native endpoint

Through the native BoothBook API, this operation is `POST /api/v1/get/bookings` (base URL `https://mindcloud.boothbook.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

