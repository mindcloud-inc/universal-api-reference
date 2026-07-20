# Instasent: Get Datasource



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource?connectionId=$CONNECTION_ID&project=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `id` | string | yes | Datasource identifier. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity.audienceTags[]` | string |  |
| `entity.createdAt` | string |  |
| `entity.defaultCountry` | string |  |
| `entity.deleted` | boolean |  |
| `entity.description` | string |  |
| `entity.id` | string |  |
| `entity.integration` | object |  |
| `entity.lastContactCreatedAt` | object |  |
| `entity.lastContactEventSyncAt` | object |  |
| `entity.lastContactExtraSyncAt` | object |  |
| `entity.lastContactGarbageCollectorSyncAt` | object |  |
| `entity.lastContactIntegratedAt` | object |  |
| `entity.lastContactReceivedAt` | object |  |
| `entity.lastContactSyncAt` | object |  |
| `entity.lastEventCreatedAt` | object |  |
| `entity.lastEventImport` | object |  |
| `entity.lastEventReceivedAt` | object |  |
| `entity.lastExtraImport` | object |  |
| `entity.lastGarbageCollectorImport` | object |  |
| `entity.lastImport` | object |  |
| `entity.locale` | string |  |
| `entity.name` | string |  |
| `entity.priority` | number |  |
| `entity.receivedContacts` | object |  |
| `entity.receivedEvents` | object |  |
| `entity.receivedIntegrations` | object |  |
| `entity.receivedIntegrationsCreations` | object |  |
| `entity.receivedIntegrationsMerges` | object |  |
| `entity.receivedIntegrationsUpdates` | object |  |
| `entity.sequence` | number |  |
| `entity.sequenceDate` | string |  |
| `entity.timezone` | string |  |
| `entity.token.callbackUrl` | object |  |
| `entity.token.createdAt` | string |  |
| `entity.token.id` | string |  |
| `entity.token.projects[]` | object |  |
| `entity.token.testMode` | boolean |  |
| `entity.token.title` | string |  |
| `entity.token.token` | string |  |
| `entity.type` | string |  |
| `entity.uid` | string |  |
| `entity.uniqueDsfield` | string |  |
| `entity.updatedAt` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/datasource/:id` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasource.md) for the provider-specific parameters and requirements.

