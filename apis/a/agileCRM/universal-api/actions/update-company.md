# Agile CRM: Update Company

Updates an existing company in Agile CRM.

```
PUT https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agile CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "4717194463870976"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "4717194463870976"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | list | yes | Example: `4717194463870976`. |
| `name` | string | no | Example: `Acme Inc`. |
| `url` | string | no | Example: `https://acme.example`. |
| `email` | string | no | Example: `ops@acme.example`. |
| `phone` | string | no | Example: `+14155550123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "concurrentSaveAllowed": true,
      "createdTime": "2026-05-07T12:00:00.000Z",
      "entityType": "string",
      "formId": 1,
      "id": 1,
      "isClientImport": true,
      "isDuplicateExisted": true,
      "isDuplicateVerificationFailed": true,
      "isLeadConverted": true,
      "kloutScore": "string",
      "lastCalled": "2026-05-07T12:00:00.000Z",
      "lastCampaignEmaild": "2026-05-07T12:00:00.000Z",
      "lastContacted": "2026-05-07T12:00:00.000Z",
      "lastEmailed": "2026-05-07T12:00:00.000Z",
      "leadConvertedTime": "2026-05-07T12:00:00.000Z",
      "leadScore": 1,
      "leadSourceId": 1,
      "leadStatusId": 1,
      "owner": {
        "calendarUrl": "https://example.com",
        "calendarURL": "https://example.com",
        "domain": "string",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "phone": "string",
        "pic": "string",
        "scheduleId": "string"
      },
      "properties": [
        {
          "name": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "restoredTime": "2026-05-07T12:00:00.000Z",
      "starValue": 1,
      "tags": [
        "string"
      ],
      "tagsWithTime": [
        {
          "availableCount": 1,
          "createdTime": "2026-05-07T12:00:00.000Z",
          "entityType": "string",
          "tag": "string"
        }
      ],
      "trashedTime": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z",
      "viewed": {
        "viewedTime": "2026-05-07T12:00:00.000Z"
      },
      "viewedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `concurrentSaveAllowed` | boolean |  |
| `createdTime` | date |  |
| `entityType` | string |  |
| `formId` | number |  |
| `id` | number |  |
| `isClientImport` | boolean |  |
| `isDuplicateExisted` | boolean |  |
| `isDuplicateVerificationFailed` | boolean |  |
| `isLeadConverted` | boolean |  |
| `kloutScore` | string |  |
| `lastCalled` | date |  |
| `lastCampaignEmaild` | date |  |
| `lastContacted` | date |  |
| `lastEmailed` | date |  |
| `leadConvertedTime` | date |  |
| `leadScore` | number |  |
| `leadSourceId` | number |  |
| `leadStatusId` | number |  |
| `owner.calendarUrl` | string |  |
| `owner.calendarURL` | string |  |
| `owner.domain` | string |  |
| `owner.email` | string |  |
| `owner.id` | number |  |
| `owner.name` | string |  |
| `owner.phone` | string |  |
| `owner.pic` | string |  |
| `owner.scheduleId` | string |  |
| `properties[].name` | string |  |
| `properties[].type` | string |  |
| `properties[].value` | string |  |
| `restoredTime` | date |  |
| `starValue` | number |  |
| `tags[]` | string |  |
| `tagsWithTime[].availableCount` | number |  |
| `tagsWithTime[].createdTime` | date |  |
| `tagsWithTime[].entityType` | string |  |
| `tagsWithTime[].tag` | string |  |
| `trashedTime` | date |  |
| `type` | string |  |
| `updatedTime` | date |  |
| `viewed.viewedTime` | date |  |
| `viewedTime` | date |  |

## Native endpoint

Through the native Agile CRM API, this operation is `PUT /contacts/edit-properties` (base URL `https://mindcloud.agilecrm.com/dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

