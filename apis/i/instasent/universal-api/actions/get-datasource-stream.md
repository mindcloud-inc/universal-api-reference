# Instasent: Get Datasource Stream



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stream
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stream?connectionId=$CONNECTION_ID&project=string&datasource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "datasource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stream?${params}`, {
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
| `datasource` | string | yes | Datasource identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datasource": {
        "audienceTags": [
          "string"
        ],
        "createdAt": "string",
        "defaultCountry": "string",
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
        "timezone": "string",
        "type": "string",
        "uid": "string",
        "updatedAt": "string"
      },
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
      "project": {
        "createdAt": "string",
        "id": "string",
        "locale": "string",
        "name": "Ava Chen",
        "timezone": "string",
        "uid": "string",
        "updatedAt": "string"
      },
      "stream": {
        "callsFailures": 1,
        "callsSuccess": 1,
        "callsTotal": 1,
        "exposed": true,
        "id": "string",
        "lastCallTime": "string",
        "lastFailureTime": {},
        "lastSuccessTime": {},
        "processedEntitiesFailures": 1,
        "processedEntitiesSuccess": 1,
        "purpose": {},
        "type": "string"
      },
      "token": {
        "scopes": [
          "string"
        ],
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasource.audienceTags[]` | string |  |
| `datasource.createdAt` | string |  |
| `datasource.defaultCountry` | string |  |
| `datasource.id` | string |  |
| `datasource.integration` | object |  |
| `datasource.lastContactCreatedAt` | string |  |
| `datasource.lastContactEventSyncAt` | object |  |
| `datasource.lastContactExtraSyncAt` | object |  |
| `datasource.lastContactGarbageCollectorSyncAt` | object |  |
| `datasource.lastContactIntegratedAt` | string |  |
| `datasource.lastContactReceivedAt` | string |  |
| `datasource.lastContactSyncAt` | object |  |
| `datasource.lastEventCreatedAt` | object |  |
| `datasource.lastEventImport` | object |  |
| `datasource.lastEventReceivedAt` | object |  |
| `datasource.lastExtraImport` | object |  |
| `datasource.lastGarbageCollectorImport` | object |  |
| `datasource.lastImport` | object |  |
| `datasource.locale` | string |  |
| `datasource.name` | string |  |
| `datasource.priority` | number |  |
| `datasource.receivedContacts` | number |  |
| `datasource.receivedEvents` | object |  |
| `datasource.receivedIntegrations` | number |  |
| `datasource.receivedIntegrationsCreations` | number |  |
| `datasource.receivedIntegrationsMerges` | object |  |
| `datasource.receivedIntegrationsUpdates` | object |  |
| `datasource.sequence` | number |  |
| `datasource.timezone` | string |  |
| `datasource.type` | string |  |
| `datasource.uid` | string |  |
| `datasource.updatedAt` | string |  |
| `organization.account.credit.currency` | string |  |
| `organization.account.credit.resetAt` | object |  |
| `organization.account.credit.resetTo` | number |  |
| `organization.account.credit.value` | number |  |
| `organization.account.funds.currency` | string |  |
| `organization.account.funds.value` | number |  |
| `organization.api.tier` | number |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `organization.plan.key` | string |  |
| `organization.plan.quality` | number |  |
| `organization.plan.status` | string |  |
| `project.createdAt` | string |  |
| `project.id` | string |  |
| `project.locale` | string |  |
| `project.name` | string |  |
| `project.timezone` | string |  |
| `project.uid` | string |  |
| `project.updatedAt` | string |  |
| `stream.callsFailures` | number |  |
| `stream.callsSuccess` | number |  |
| `stream.callsTotal` | number |  |
| `stream.exposed` | boolean |  |
| `stream.id` | string |  |
| `stream.lastCallTime` | string |  |
| `stream.lastFailureTime` | object |  |
| `stream.lastSuccessTime` | object |  |
| `stream.processedEntitiesFailures` | number |  |
| `stream.processedEntitiesSuccess` | number |  |
| `stream.purpose` | object |  |
| `stream.type` | string |  |
| `token.scopes[]` | string |  |
| `token.type` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/datasource/:datasource/stream` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasource-stream.md) for the provider-specific parameters and requirements.

