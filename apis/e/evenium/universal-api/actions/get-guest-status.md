# Evenium: Get Guest Status

Retrieves a guest status from Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-guest-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-guest-status?connectionId=$CONNECTION_ID&contactId=1&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1",
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-guest-status?${params}`, {
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
| `contactId` | number | yes | The Evenium Contact ID. |
| `eventId` | number | yes | The Evenium Event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "eventId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number | Guest contact ID. |
| `eventId` | number | Parent event ID. |
| `status` | string | Guest status value. |

## Native endpoint

Through the native Evenium API, this operation is `GET /events/:eventId/guests/:contactId/status` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-guest-status.md) for the provider-specific parameters and requirements.

