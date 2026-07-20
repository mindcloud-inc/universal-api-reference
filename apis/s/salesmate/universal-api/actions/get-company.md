# Salesmate: Get Company



```
GET https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-company?${params}`, {
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
| `companyId` | number | yes | Salesmate company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annualRevenue": 1,
      "associatedContacts": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "description": "string",
      "emailOptOut": true,
      "id": 1,
      "imagePath": "string",
      "lastCommunicationAt": "2026-05-07T12:00:00.000Z",
      "lastCommunicationBy": "string",
      "lastCommunicationMode": "string",
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "lastModifiedBy": {},
      "lastNote": "string",
      "lastNoteAddedAt": "2026-05-07T12:00:00.000Z",
      "lastNoteAddedBy": {},
      "lostDealCount": 1,
      "name": "Ava Chen",
      "numberOfEmployees": 1,
      "openActivities": 1,
      "openDealCount": 1,
      "otherPhone": "string",
      "owner": {},
      "phone": "string",
      "photo": "string",
      "smsOptOut": true,
      "tags": "string",
      "totalActivities": 1,
      "totalAmountOfLostDeal": 1,
      "totalAmountOfOpenDeal": 1,
      "totalAmountOfWonDeal": 1,
      "type": "string",
      "website": "string",
      "wonDealCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annualRevenue` | number |  |
| `associatedContacts` | number |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `description` | string |  |
| `emailOptOut` | boolean |  |
| `id` | number |  |
| `imagePath` | string |  |
| `lastCommunicationAt` | date |  |
| `lastCommunicationBy` | string |  |
| `lastCommunicationMode` | string |  |
| `lastModifiedAt` | date |  |
| `lastModifiedBy` | object |  |
| `lastNote` | string |  |
| `lastNoteAddedAt` | date |  |
| `lastNoteAddedBy` | object |  |
| `lostDealCount` | number |  |
| `name` | string |  |
| `numberOfEmployees` | number |  |
| `openActivities` | number |  |
| `openDealCount` | number |  |
| `otherPhone` | string |  |
| `owner` | object |  |
| `phone` | string |  |
| `photo` | string |  |
| `smsOptOut` | boolean |  |
| `tags` | string |  |
| `totalActivities` | number |  |
| `totalAmountOfLostDeal` | number |  |
| `totalAmountOfOpenDeal` | number |  |
| `totalAmountOfWonDeal` | number |  |
| `type` | string |  |
| `website` | string |  |
| `wonDealCount` | number |  |

## Native endpoint

Through the native Salesmate API, this operation is `GET /company/v4/:companyId` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

