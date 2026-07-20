# Instasent Universal API Examples

These examples use the MindCloud API key and Instasent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-projects?${params}`, {
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
      "entity": {
        "callbackUrl": {},
        "createdAt": "string",
        "id": "string",
        "projects": [
          {
            "attributionConfig": {},
            "brand": {},
            "businessContactsSize": {},
            "businessType": "string",
            "businessUrl": {},
            "conversionConfig": {},
            "createdAt": "string",
            "defaultSmsSender": {},
            "description": "string",
            "generalConfig": {},
            "id": "string",
            "locale": "string",
            "lockedReason": {},
            "lockedUntil": {},
            "name": "Ava Chen",
            "projectStatus": "string",
            "projectType": "string",
            "shortTrackingDomain": {},
            "timezone": "string",
            "uid": "string",
            "unsubscribeTrackingDomain": {},
            "updatedAt": "string"
          }
        ],
        "support": [
          "string"
        ],
        "testMode": true,
        "title": "string",
        "token": "string"
      },
      "metadata": {
        "organization": {
          "account": {
            "credit": {
              "currency": "string",
              "resetAt": {},
              "resetTo": 1,
              "value": 1
            },
            "funds": {
              "currency": "string",
              "value": 1
            }
          },
          "api": {
            "tier": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "plan": {
            "key": "string",
            "quality": 1,
            "status": "string"
          }
        },
        "scopes": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instasent/latest/actions/list-projects).

## Create Datasource



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/create-datasource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "name": "Ava Chen",
  "audienceTags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instasent/latest/actions/create-datasource', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "name": "Ava Chen",
    "audienceTags[]": ["string"]
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
      "entity": {
        "audienceTags": [
          "string"
        ],
        "createdAt": "string",
        "defaultCountry": "string",
        "deleted": true,
        "description": "string",
        "id": "string",
        "integration": {},
        "lastContactCreatedAt": {},
        "lastContactEventSyncAt": {},
        "lastContactExtraSyncAt": {},
        "lastContactGarbageCollectorSyncAt": {},
        "lastContactIntegratedAt": {},
        "lastContactReceivedAt": {},
        "lastContactSyncAt": {},
        "lastEventCreatedAt": {},
        "lastEventImport": {},
        "lastEventReceivedAt": {},
        "lastExtraImport": {},
        "lastGarbageCollectorImport": {},
        "lastImport": {},
        "locale": "string",
        "name": "Ava Chen",
        "priority": 1,
        "projectAttributeMappings": {},
        "receivedContacts": {},
        "receivedEvents": {},
        "receivedIntegrations": {},
        "receivedIntegrationsCreations": {},
        "receivedIntegrationsMerges": {},
        "receivedIntegrationsUpdates": {},
        "sequence": 1,
        "sequenceDate": "string",
        "timezone": "string",
        "token": {
          "callbackUrl": {},
          "createdAt": "string",
          "id": "string",
          "projects": [
            {}
          ],
          "testMode": true,
          "title": "string",
          "token": "string"
        },
        "type": "string",
        "uid": "string",
        "uniqueDsfield": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Datasource action reference](actions/create-datasource.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instasent/latest/actions/create-datasource).
