# Previsto: Update Service Agreement

Updates an existing service agreement in Previsto.

```
PUT https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-service-agreement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-service-agreement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-service-agreement', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Previsto service agreement ID. |
| `description` | string | no | Updated service agreement description. |

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

Through the native Previsto API, this operation is `PUT /agreements/:id` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service-agreement.md) for the provider-specific parameters and requirements.

