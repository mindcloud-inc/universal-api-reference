# Let's Calendar: Update Campaign Invites

Updates and sends calendar invites in Let's Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/update-campaign-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/update-campaign-invites" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/update-campaign-invites', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The unique identifier of the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `POST update-invite` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign-invites.md) for the provider-specific parameters and requirements.

