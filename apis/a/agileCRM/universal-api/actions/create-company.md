# Agile CRM: Create Company

Creates a new company in Agile CRM.

```
POST https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agile CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Acme Inc"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Acme Inc"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Example: `Acme Inc`. |
| `email` | string | no | Example: `sales@acme.com`. |
| `phone` | string | no | Example: `+14155550111`. |
| `url` | string | no | Example: `https://acme.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags[]` | array<string> | no |  |
| `leadScore` | number | no | Lead score value for the company record. |
| `starValue` | number | no | Star value for company prioritization. |

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
      "source": "string",
      "starValue": 1,
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
| `source` | string |  |
| `starValue` | number |  |
| `trashedTime` | date |  |
| `type` | string |  |
| `updatedTime` | date |  |
| `viewed.viewedTime` | date |  |
| `viewedTime` | date |  |

## Native endpoint

Through the native Agile CRM API, this operation is `POST /contacts` (base URL `https://mindcloud.agilecrm.com/dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

