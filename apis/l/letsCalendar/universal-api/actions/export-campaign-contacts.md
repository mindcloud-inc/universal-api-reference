# Let's Calendar: Export Campaign Contacts

Exports campaign contacts from Let's Calendar.

```
GET https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/export-campaign-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/export-campaign-contacts?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/export-campaign-contacts?${params}`, {
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
| `campaignId` | string | yes | The unique identifier of the campaign to export contacts from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignName": "Ava Chen",
      "downloadUrl": "https://example.com",
      "exportTimestamp": "string",
      "message": "string",
      "totalContacts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignName` | string |  |
| `downloadUrl` | string |  |
| `exportTimestamp` | string |  |
| `message` | string |  |
| `totalContacts` | number |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `GET campaign/:campaignId/export-contacts` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-campaign-contacts.md) for the provider-specific parameters and requirements.

