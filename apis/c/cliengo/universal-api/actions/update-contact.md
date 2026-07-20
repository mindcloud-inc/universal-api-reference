# Cliengo: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Identifier of the Cliengo contact. |
| `name` | string | no | Contact name. |
| `email` | string | no | Contact email. |
| `phone` | string | no | Contact phone number. |
| `status` | string | no | Contact status. Possible values include NEW, ACTIVE, LONG_TERM, and CLIENT. |
| `subStatus` | string | no | Contact sub-status. |
| `rating` | number | no | Contact rating from 0 to 5. |
| `assignedTo` | string | no | User ID to assign the contact to, or UNASSIGNED. |
| `dueDate` | date | no | Scheduled due date for the contact. |
| `contactMethod` | string | no | Entry method such as WHATSAPP, FB_LEADADS, FORM, CHATBOT, API, or ZAPIER. |
| `note` | string | no | Simple note stored on the contact log. |
| `scheduleStatusTo` | string | no | Future status to apply on the scheduled date. |
| `scheduleDate` | date | no | Date when the scheduled status should replace the current status. |
| `sellPrice` | number | no | Contact sell price. |
| `sellSuscription` | string | no | Sell subscription type such as ONE_TIME, MONTHLY_SUSCRIPTION, YEARLY_SUSCRIPTION, or OTHER_SELL_TYPE. |
| `cancelReason` | string | no | Cancellation reason code from 1 to 5. |
| `extraParams` | object | no | Additional custom parameters object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "age": 1,
      "calls": [
        "string"
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "duplicatedContact": true,
      "email": "ava@example.com",
      "entryMethod": "string",
      "geoip": {},
      "id": "string",
      "lastName": "Chen",
      "lastUpdateDate": "2026-05-07T12:00:00.000Z",
      "leadFields": {},
      "logs": [
        "string"
      ],
      "medium": "string",
      "mediumTranslate": "string",
      "message": "string",
      "name": "Ava Chen",
      "notes": [
        "string"
      ],
      "phone": "string",
      "rating": 1,
      "status": "string",
      "subStatus": "string",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmTerm": "string",
      "websiteId": "string",
      "websiteName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountName` | string |  |
| `age` | number |  |
| `calls` | array |  |
| `creationDate` | date |  |
| `duplicatedContact` | boolean |  |
| `email` | string |  |
| `entryMethod` | string |  |
| `geoip` | object |  |
| `id` | string |  |
| `lastName` | string |  |
| `lastUpdateDate` | date |  |
| `leadFields` | object |  |
| `logs` | array |  |
| `medium` | string |  |
| `mediumTranslate` | string |  |
| `message` | string |  |
| `name` | string |  |
| `notes` | array |  |
| `phone` | string |  |
| `rating` | number |  |
| `status` | string |  |
| `subStatus` | string |  |
| `utmCampaign` | string |  |
| `utmContent` | string |  |
| `utmMedium` | string |  |
| `utmTerm` | string |  |
| `websiteId` | string |  |
| `websiteName` | string |  |

## Native endpoint

Through the native Cliengo API, this operation is `PATCH /contacts/:contactId` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

