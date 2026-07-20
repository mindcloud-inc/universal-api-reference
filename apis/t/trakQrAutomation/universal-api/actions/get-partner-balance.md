# Trak Qr Automation: Get Partner Balance

Retrieves partner balance from Trak Qr Automation.

```
GET https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/get-partner-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trak Qr Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/get-partner-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/get-partner-balance?${params}`, {
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
| `startDate` | date | no | Optional attendee creation start date, inclusive, in ISO 8601 format. |
| `endDate` | date | no | Optional attendee creation end date, exclusive, in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendeesCount": 1,
      "eventId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendeesCount` | number | Number of attendees created so far. |
| `eventId` | string | Internal event ID used as correlation ID. |
| `title` | string | Event title. |

## Native endpoint

Through the native Trak Qr Automation API, this operation is `GET /events-partners/balance` (base URL `https://backend.trak.codes/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-partner-balance.md) for the provider-specific parameters and requirements.

