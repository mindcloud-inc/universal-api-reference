# Salesmate: Get Deal



```
GET https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-deal?connectionId=$CONNECTION_ID&dealId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-deal?${params}`, {
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
| `dealId` | number | yes | Salesmate deal ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closedDate": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "currency": {},
      "dealValue": 1,
      "description": "string",
      "estimatedCloseDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDeleted": true,
      "isSplitted": true,
      "lastActivityAt": "2026-05-07T12:00:00.000Z",
      "lastActivityBy": {},
      "lastCommunicationAt": "2026-05-07T12:00:00.000Z",
      "lastCommunicationBy": "string",
      "lastCommunicationMode": "string",
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "lastModifiedBy": {},
      "lastNote": "string",
      "lastNoteAddedAt": "2026-05-07T12:00:00.000Z",
      "lastNoteAddedBy": {},
      "owner": {},
      "pipeline": "string",
      "primaryCompany": {},
      "primaryContact": {},
      "priority": "string",
      "rottenDate": "2026-05-07T12:00:00.000Z",
      "source": "string",
      "stage": "string",
      "status": "string",
      "tags": "string",
      "title": "string",
      "winProbability": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closedDate` | date |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `currency` | object |  |
| `dealValue` | number |  |
| `description` | string |  |
| `estimatedCloseDate` | date |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `isSplitted` | boolean |  |
| `lastActivityAt` | date |  |
| `lastActivityBy` | object |  |
| `lastCommunicationAt` | date |  |
| `lastCommunicationBy` | string |  |
| `lastCommunicationMode` | string |  |
| `lastModifiedAt` | date |  |
| `lastModifiedBy` | object |  |
| `lastNote` | string |  |
| `lastNoteAddedAt` | date |  |
| `lastNoteAddedBy` | object |  |
| `owner` | object |  |
| `pipeline` | string |  |
| `primaryCompany` | object |  |
| `primaryContact` | object |  |
| `priority` | string |  |
| `rottenDate` | date |  |
| `source` | string |  |
| `stage` | string |  |
| `status` | string |  |
| `tags` | string |  |
| `title` | string |  |
| `winProbability` | number |  |

## Native endpoint

Through the native Salesmate API, this operation is `GET /deal/v4/:dealId` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

