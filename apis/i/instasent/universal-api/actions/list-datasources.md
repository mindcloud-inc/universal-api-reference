# Instasent: List Datasources



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-datasources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-datasources?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-datasources?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {
          "audienceTags": [
            "string"
          ],
          "createdAt": "string",
          "defaultCountry": "string",
          "deleted": true,
          "description": "string",
          "id": "string",
          "integration": {},
          "lastContactCreatedAt": "string",
          "lastContactEventSyncAt": {},
          "lastContactExtraSyncAt": {},
          "lastContactGarbageCollectorSyncAt": {},
          "lastContactIntegratedAt": "string",
          "lastContactReceivedAt": "string",
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
          "receivedContacts": 1,
          "receivedEvents": {},
          "receivedIntegrations": 1,
          "receivedIntegrationsCreations": 1,
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
      ],
      "metadata": {
        "count": 1,
        "limit": 1,
        "start": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities[].audienceTags[]` | string |  |
| `entities[].createdAt` | string |  |
| `entities[].defaultCountry` | string |  |
| `entities[].deleted` | boolean |  |
| `entities[].description` | string |  |
| `entities[].id` | string |  |
| `entities[].integration` | object |  |
| `entities[].lastContactCreatedAt` | string |  |
| `entities[].lastContactEventSyncAt` | object |  |
| `entities[].lastContactExtraSyncAt` | object |  |
| `entities[].lastContactGarbageCollectorSyncAt` | object |  |
| `entities[].lastContactIntegratedAt` | string |  |
| `entities[].lastContactReceivedAt` | string |  |
| `entities[].lastContactSyncAt` | object |  |
| `entities[].lastEventCreatedAt` | object |  |
| `entities[].lastEventImport` | object |  |
| `entities[].lastEventReceivedAt` | object |  |
| `entities[].lastExtraImport` | object |  |
| `entities[].lastGarbageCollectorImport` | object |  |
| `entities[].lastImport` | object |  |
| `entities[].locale` | string |  |
| `entities[].name` | string |  |
| `entities[].priority` | number |  |
| `entities[].receivedContacts` | number |  |
| `entities[].receivedEvents` | object |  |
| `entities[].receivedIntegrations` | number |  |
| `entities[].receivedIntegrationsCreations` | number |  |
| `entities[].receivedIntegrationsMerges` | object |  |
| `entities[].receivedIntegrationsUpdates` | object |  |
| `entities[].sequence` | number |  |
| `entities[].sequenceDate` | string |  |
| `entities[].timezone` | string |  |
| `entities[].token.callbackUrl` | object |  |
| `entities[].token.createdAt` | string |  |
| `entities[].token.id` | string |  |
| `entities[].token.projects[]` | object |  |
| `entities[].token.testMode` | boolean |  |
| `entities[].token.title` | string |  |
| `entities[].token.token` | string |  |
| `entities[].type` | string |  |
| `entities[].uid` | string |  |
| `entities[].uniqueDsfield` | string |  |
| `entities[].updatedAt` | string |  |
| `metadata.count` | number |  |
| `metadata.limit` | number |  |
| `metadata.start` | number |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/datasource` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasources.md) for the provider-specific parameters and requirements.

