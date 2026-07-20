# Zoho Calendar: Share Calendar

Updates calendar sharing in Zoho Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/share-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/share-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarUid": "string",
  "shareData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/share-calendar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarUid": "string",
    "shareData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calendarUid` | string | yes | Calendar unique identifier. |
| `shareData` | object | yes | Share payload object describing the permissions to apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "share": [
        {
          "message": "string",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `share[].message` | string |  |
| `share[].status` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `PUT /calendars/:calendaruid/share` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-calendar.md) for the provider-specific parameters and requirements.

