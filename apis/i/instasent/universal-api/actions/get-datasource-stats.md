# Instasent: Get Datasource Stats



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stats?connectionId=$CONNECTION_ID&project=string&datasource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "datasource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stats?${params}`, {
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
      "contacts": {
        "errored": 1,
        "total": 1
      },
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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts.errored` | number |  |
| `contacts.total` | number |  |
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

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/datasource/:datasource/stats` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasource-stats.md) for the provider-specific parameters and requirements.

