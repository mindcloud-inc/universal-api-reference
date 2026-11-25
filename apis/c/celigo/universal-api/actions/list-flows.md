# Celigo: List Flows



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-flows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-flows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-flows?${params}`, {
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
| `integrationId` | list<string> | no | Only return flows in this integration. |
| `name` | string | no | Only return flows whose name contains this text (case-insensitive). |
| `disabled` | boolean | no | Only return disabled (true) or enabled (false) flows. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | list<string> | no | Sort by most recent execution; never-run flows come last. One of: `lastExecutedAt`. |
| `order` | list<string> | no | Sort direction. One of: `asc`, `desc`. |
| `externalId` | string | no | Only return flows with this exact external identifier. |
| `includeInstances` | boolean | no | Also return instance flows generated from multi-instance (abstract) flows. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiDescription": {},
      "autoResolveMatchingTraceKeys": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "disabled": true,
      "free": true,
      "id": "string",
      "integrationId": "string",
      "lastExecutedAt": "2026-05-07T12:00:00.000Z",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "logging": {},
      "name": "Ava Chen",
      "pageGenerators": [
        {
          "exportId": "string",
          "skipRetries": true
        }
      ],
      "pageProcessors": [
        {
          "exportId": "string",
          "hooks": {
            "postResponseMap": {}
          },
          "importId": "string",
          "proceedOnFailure": true,
          "responseMapping": {
            "fields": [
              {}
            ],
            "lists": [
              "string"
            ]
          },
          "type": "string"
        }
      ],
      "runNextFlowIds": [
        "string"
      ],
      "runPageGeneratorsInParallel": true,
      "schedule": "string",
      "sourceId": "string",
      "templateId": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiDescription` | object |  |
| `autoResolveMatchingTraceKeys` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `free` | boolean |  |
| `id` | string |  |
| `integrationId` | string |  |
| `lastExecutedAt` | date |  |
| `lastModified` | date |  |
| `logging` | object |  |
| `name` | string |  |
| `pageGenerators` | array<object> |  |
| `pageGenerators[].exportId` | string |  |
| `pageGenerators[].skipRetries` | boolean |  |
| `pageProcessors` | array<object> |  |
| `pageProcessors[].exportId` | string |  |
| `pageProcessors[].hooks` | object |  |
| `pageProcessors[].hooks.postResponseMap` | object |  |
| `pageProcessors[].importId` | string |  |
| `pageProcessors[].proceedOnFailure` | boolean |  |
| `pageProcessors[].responseMapping` | object |  |
| `pageProcessors[].responseMapping.fields` | array<object> |  |
| `pageProcessors[].responseMapping.lists` | array |  |
| `pageProcessors[].type` | string |  |
| `runNextFlowIds` | array<string> |  |
| `runPageGeneratorsInParallel` | boolean |  |
| `schedule` | string |  |
| `sourceId` | string |  |
| `templateId` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /flows` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-flows.md) for the provider-specific parameters and requirements.

