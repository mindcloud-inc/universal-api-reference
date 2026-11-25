# Celigo: Get Flow



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-flow?connectionId=$CONNECTION_ID&flowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "flowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-flow?${params}`, {
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
| `flowId` | list<string> | yes | Flow to get. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mergeInstance` | boolean | no | For an instance of a multi-instance flow, merge in the abstract flow configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoResolveMatchingTraceKeys": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
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
      "runPageGeneratorsInParallel": true,
      "schedule": "string",
      "sourceId": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoResolveMatchingTraceKeys` | boolean |  |
| `createdAt` | date |  |
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
| `pageProcessors[].responseMapping` | object |  |
| `pageProcessors[].responseMapping.fields` | array<object> |  |
| `pageProcessors[].responseMapping.lists` | array |  |
| `pageProcessors[].type` | string |  |
| `runPageGeneratorsInParallel` | boolean |  |
| `schedule` | string |  |
| `sourceId` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /flows/:flowId` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flow.md) for the provider-specific parameters and requirements.

