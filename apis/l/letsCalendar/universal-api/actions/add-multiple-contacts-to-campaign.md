# Let's Calendar: Add Multiple Contacts to Campaign

Adds multiple contacts to a campaign in Let's Calendar.

```
POST https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/add-multiple-contacts-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/add-multiple-contacts-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "contacts[].firstname": "Ava",
  "contacts[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/add-multiple-contacts-to-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "contacts[].firstname": "Ava",
    "contacts[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The unique identifier of the campaign. |
| `contacts[]` | array<object> | no | Array of contacts to add to the campaign. |
| `contacts[].firstname` | string | yes | The first name of the contact. |
| `contacts[].lastname` | string | no | The last name of the contact. |
| `contacts[].email` | string | yes | A valid email address. |
| `contacts[].loginurl` | string | no | The login URL for the contact. |
| `contacts[].username` | string | no | The username for the contact. |
| `contacts[].password` | string | no | The password for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duplicateCount": 1,
      "duplicateEmails": [
        [
          "ava@example.com"
        ]
      ],
      "invalidCount": 1,
      "message": "string",
      "validCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duplicateCount` | number |  |
| `duplicateEmails[]` | array<string> |  |
| `invalidCount` | number |  |
| `message` | string |  |
| `validCount` | number |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `POST add-contacts` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-multiple-contacts-to-campaign.md) for the provider-specific parameters and requirements.

