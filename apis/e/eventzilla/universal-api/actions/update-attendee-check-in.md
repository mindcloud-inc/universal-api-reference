# Eventzilla: Update Attendee Check-In

Updates attendee check-in status in Eventzilla.

```
PUT https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/update-attendee-check-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/update-attendee-check-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "barcode": "string",
  "eventCheckIn": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/update-attendee-check-in', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "barcode": "string",
    "eventCheckIn": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `barcode` | string | yes |  |
| `eventCheckIn` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkinstatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkinstatus` | object |  |

## Native endpoint

Through the native Eventzilla API, this operation is `POST /attendees/checkin` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-attendee-check-in.md) for the provider-specific parameters and requirements.

