# Galileo: Get Experiment

Retrieves an experiment from Galileo by ID.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-experiment?connectionId=$CONNECTION_ID&experimentId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experimentId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-experiment?${params}`, {
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
| `experimentId` | string | yes | Galileo experiment UUID. |
| `projectId` | string | yes | Galileo project UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregateFeedback": {},
      "aggregateMetrics": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByUser": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen"
      },
      "dataset": {
        "datasetId": "string",
        "name": "Ava Chen",
        "versionIndex": 1
      },
      "id": "string",
      "name": "Ava Chen",
      "numSpans": 1,
      "numTraces": 1,
      "playground": {
        "name": "Ava Chen",
        "playgroundId": "string"
      },
      "playgroundId": "string",
      "projectId": "string",
      "prompt": {
        "content": "string",
        "name": "Ava Chen",
        "promptTemplateId": "string",
        "versionIndex": 1
      },
      "promptModel": "string",
      "promptRunSettings": {
        "deploymentName": "Ava Chen",
        "echo": true,
        "frequencyPenalty": 1,
        "logprobs": true,
        "maxTokens": 1,
        "modelAlias": "string",
        "n": 1,
        "presencePenalty": 1,
        "reasoningEffort": "string",
        "responseFormat": {},
        "stopSequences": [
          "string"
        ],
        "temperature": 1,
        "toolChoice": "string",
        "tools": "string",
        "topK": 1,
        "topLogprobs": 1,
        "topP": 1,
        "verbosity": "string"
      },
      "rank": 1,
      "rankingScore": 1,
      "ratingAggregates": {},
      "status": {
        "logGeneration": {
          "progressPercent": 1
        }
      },
      "structuredAggregateMetrics": {},
      "tags": {},
      "taskType": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "winner": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregateFeedback` | object |  |
| `aggregateMetrics` | object |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByUser.email` | string |  |
| `createdByUser.firstName` | string |  |
| `createdByUser.id` | string |  |
| `createdByUser.lastName` | string |  |
| `dataset.datasetId` | string |  |
| `dataset.name` | string |  |
| `dataset.versionIndex` | number |  |
| `id` | string |  |
| `name` | string |  |
| `numSpans` | number |  |
| `numTraces` | number |  |
| `playground.name` | string |  |
| `playground.playgroundId` | string |  |
| `playgroundId` | string |  |
| `projectId` | string |  |
| `prompt.content` | string |  |
| `prompt.name` | string |  |
| `prompt.promptTemplateId` | string |  |
| `prompt.versionIndex` | number |  |
| `promptModel` | string |  |
| `promptRunSettings.deploymentName` | string |  |
| `promptRunSettings.echo` | boolean |  |
| `promptRunSettings.frequencyPenalty` | number |  |
| `promptRunSettings.logprobs` | boolean |  |
| `promptRunSettings.maxTokens` | number |  |
| `promptRunSettings.modelAlias` | string |  |
| `promptRunSettings.n` | number |  |
| `promptRunSettings.presencePenalty` | number |  |
| `promptRunSettings.reasoningEffort` | string |  |
| `promptRunSettings.responseFormat` | object |  |
| `promptRunSettings.stopSequences` | array<string> |  |
| `promptRunSettings.temperature` | number |  |
| `promptRunSettings.toolChoice` | string |  |
| `promptRunSettings.tools` | string |  |
| `promptRunSettings.topK` | number |  |
| `promptRunSettings.topLogprobs` | number |  |
| `promptRunSettings.topP` | number |  |
| `promptRunSettings.verbosity` | string |  |
| `rank` | number |  |
| `rankingScore` | number |  |
| `ratingAggregates` | object |  |
| `status.logGeneration.progressPercent` | number |  |
| `structuredAggregateMetrics` | object |  |
| `tags` | object |  |
| `taskType` | number |  |
| `updatedAt` | date |  |
| `winner` | boolean |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id/experiments/:experiment_id` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment.md) for the provider-specific parameters and requirements.

