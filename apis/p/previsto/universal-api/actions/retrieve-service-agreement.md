# Previsto: Retrieve Service Agreement

Retrieves a service agreement from Previsto.

```
GET https://connect.mindcloud.co/v1/universal/previsto/latest/actions/retrieve-service-agreement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/retrieve-service-agreement?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/previsto/latest/actions/retrieve-service-agreement?${params}`, {
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
| `id` | string | yes | Previsto service agreement ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "amount": 1,
      "archived": true,
      "completionDuePeriod": {},
      "contactId": "string",
      "createdBy": "string",
      "createdDate": "string",
      "description": "string",
      "duration": 1,
      "endDate": {},
      "flexibleRecurrence": true,
      "id": "string",
      "lastModifiedBy": "string",
      "lastModifiedDate": "string",
      "message": {},
      "note": {},
      "planningDate": {},
      "planningDateType": "string",
      "planningTime": {},
      "priorMessage": {},
      "recurrenceRule": {},
      "stage": "string",
      "type": "string",
      "workType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `amount` | number |  |
| `archived` | boolean |  |
| `completionDuePeriod` | object |  |
| `contactId` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `endDate` | object |  |
| `flexibleRecurrence` | boolean |  |
| `id` | string |  |
| `lastModifiedBy` | string |  |
| `lastModifiedDate` | string |  |
| `message` | object |  |
| `note` | object |  |
| `planningDate` | object |  |
| `planningDateType` | string |  |
| `planningTime` | object |  |
| `priorMessage` | object |  |
| `recurrenceRule` | object |  |
| `stage` | string |  |
| `type` | string |  |
| `workType` | string |  |

## Native endpoint

Through the native Previsto API, this operation is `GET /agreements/:id` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-service-agreement.md) for the provider-specific parameters and requirements.

