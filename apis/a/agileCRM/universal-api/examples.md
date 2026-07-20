# Agile CRM Universal API Examples

These examples use the MindCloud API key and Agile CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Finds contacts in Agile CRM by filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "concurrentSaveAllowed": true,
      "contactCompanyId": "string",
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

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agileCRM/latest/actions/list-contacts).

## Create Company

Creates a new company in Agile CRM.

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

Example response:

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

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agileCRM/latest/actions/create-company).
