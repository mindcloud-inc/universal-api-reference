# Aloware: Lookup Contact By Phone Number

Finds a contact in Aloware by phone number.

```
GET https://connect.mindcloud.co/v1/universal/aloware/latest/actions/lookup-contact-by-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/lookup-contact-by-phone-number?connectionId=$CONNECTION_ID&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aloware/latest/actions/lookup-contact-by-phone-number?${params}`, {
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
| `phoneNumber` | string | yes | Phone number of the contact you want to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "campaignIds": [
        "string"
      ],
      "cnamCity": "string",
      "cnamCountry": "string",
      "cnamSource": {},
      "cnamState": "string",
      "cnamZipcode": {},
      "companyId": 1,
      "companyName": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customLink": {},
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "dispositionStatusId": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "inboundCallCount": 1,
      "inboundSmsCount": 1,
      "initialCampaignId": {},
      "intakeSource": "string",
      "integrationData": {},
      "isBlocked": true,
      "isDnc": true,
      "lastEngagementAt": "2026-05-07T12:00:00.000Z",
      "lastEngagementText": "string",
      "lastName": "Chen",
      "leadSource": "string",
      "leadSourceId": {},
      "lrnType": 1,
      "name": "Ava Chen",
      "nbCommunications": 1,
      "notes": "string",
      "outboundCallCount": 1,
      "outboundSmsCount": 1,
      "phoneNumber": "string",
      "sequenceId": {},
      "tags": [
        "string"
      ],
      "textAuthorized": 1,
      "textAuthorizedAt": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "unreadCount": 1,
      "unreadMissedCallCount": 1,
      "unreadVoicemailCount": 1,
      "userId": {},
      "uuidV4": "string",
      "website": {},
      "workflowId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `campaignIds` | array |  |
| `cnamCity` | string |  |
| `cnamCountry` | string |  |
| `cnamSource` | object |  |
| `cnamState` | string |  |
| `cnamZipcode` | object |  |
| `companyId` | number |  |
| `companyName` | object |  |
| `createdAt` | date |  |
| `customLink` | object |  |
| `dateOfBirth` | date |  |
| `dispositionStatusId` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `inboundCallCount` | number |  |
| `inboundSmsCount` | number |  |
| `initialCampaignId` | object |  |
| `intakeSource` | string |  |
| `integrationData` | object |  |
| `isBlocked` | boolean |  |
| `isDnc` | boolean |  |
| `lastEngagementAt` | date |  |
| `lastEngagementText` | string |  |
| `lastName` | string |  |
| `leadSource` | string |  |
| `leadSourceId` | object |  |
| `lrnType` | number |  |
| `name` | string |  |
| `nbCommunications` | number |  |
| `notes` | string |  |
| `outboundCallCount` | number |  |
| `outboundSmsCount` | number |  |
| `phoneNumber` | string |  |
| `sequenceId` | object |  |
| `tags` | array |  |
| `textAuthorized` | number |  |
| `textAuthorizedAt` | date |  |
| `timezone` | string |  |
| `unreadCount` | number |  |
| `unreadMissedCallCount` | number |  |
| `unreadVoicemailCount` | number |  |
| `userId` | object |  |
| `uuidV4` | string |  |
| `website` | object |  |
| `workflowId` | object |  |

## Native endpoint

Through the native Aloware API, this operation is `GET /api/v1/webhook/contact/phone-number` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-contact-by-phone-number.md) for the provider-specific parameters and requirements.

