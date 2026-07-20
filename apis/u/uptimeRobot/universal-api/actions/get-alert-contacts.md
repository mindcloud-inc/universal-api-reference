# UptimeRobot: Get Alert Contacts

Retrieves alert contacts and details from UptimeRobot.

```
GET https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-alert-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UptimeRobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-alert-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-alert-contacts?${params}`, {
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
| `alert_contacts` | string | no | Optional dash-separated alert contact IDs to filter. |
| `offset` | number | no | Pagination offset. |
| `limit` | number | no | Pagination limit, max 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert_contacts": [
        {}
      ],
      "limit": 1,
      "offset": 1,
      "stat": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_contacts` | array<object> |  |
| `limit` | number |  |
| `offset` | number |  |
| `stat` | string |  |
| `total` | number |  |

## Native endpoint

Through the native UptimeRobot API, this operation is `POST /getAlertContacts` (base URL `https://api.uptimerobot.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert-contacts.md) for the provider-specific parameters and requirements.

