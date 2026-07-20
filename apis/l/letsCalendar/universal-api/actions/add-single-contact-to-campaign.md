# Let's Calendar: Add Single Contact to Campaign

Adds a contact to a campaign in Let's Calendar.

```
POST https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/add-single-contact-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/add-single-contact-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "firstname": "Ava",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/add-single-contact-to-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "firstname": "Ava",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The unique identifier of the campaign. |
| `firstname` | string | yes | The first name of the contact. |
| `lastname` | string | no | The last name of the contact. |
| `email` | string | yes | A valid email address. |
| `loginurl` | string | no | The login URL for the contact. |
| `username` | string | no | The username for the contact. |
| `password` | string | no | The password for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `POST add-single-contact` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-single-contact-to-campaign.md) for the provider-specific parameters and requirements.

