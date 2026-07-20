# Previsto Universal API Examples

These examples use the MindCloud API key and Previsto connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from Previsto.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/previsto/latest/actions/list-organizations?${params}`, {
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
      "address": "string",
      "apiVersion": "string",
      "appartment": {},
      "baseCurrency": "string",
      "city": "string",
      "countryCode": "string",
      "createdBy": "string",
      "createdDate": "string",
      "email": "ava@example.com",
      "id": "string",
      "languageCode": "string",
      "lastModifiedBy": "string",
      "lastModifiedDate": "string",
      "location": [
        1
      ],
      "name": "Ava Chen",
      "phone": {},
      "postalCode": "string",
      "registrationNo": {},
      "taxRates": [
        {
          "rate": 1,
          "workType": "string"
        }
      ],
      "timeZone": "string",
      "url": {}
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/previsto/latest/actions/list-organizations).

## Create Assignment

Creates a new assignment in Previsto.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/create-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "accountId": "string",
  "location": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/previsto/latest/actions/create-assignment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "accountId": "string",
    "location": "string"
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
      "accountId": "string",
      "action": "string",
      "address": {
        "apartment": {},
        "city": "string",
        "countryCode": "string",
        "postalCode": "string",
        "street": "string"
      },
      "contactId": "string",
      "contactName": "Ava Chen",
      "createdBy": "string",
      "createdDate": "string",
      "deliveryAddress": {},
      "flagged": true,
      "handledDate": {},
      "id": "string",
      "lastModifiedBy": "string",
      "lastModifiedDate": "string",
      "location": [
        1
      ],
      "locationResolvementStatus": "string",
      "message": {},
      "notifiedOfImpendingWork": true,
      "payingContactId": {},
      "plan": {
        "affixment": {
          "link": {},
          "state": "string"
        },
        "allDay": true,
        "completionDuePeriod": {},
        "completionDueTime": {},
        "executionTime": "string",
        "indicativeDate": {},
        "indicativeDateType": "string",
        "mode": "string",
        "serviceWindow": {},
        "specificStartTime": true
      },
      "remoteOrderId": {},
      "sentState": "string",
      "stateId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Assignment action reference](actions/create-assignment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/previsto/latest/actions/create-assignment).
