# Langfuse: List Observations

Retrieves observations from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-observations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-observations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-observations?${params}`, {
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
| `cursor` | string | no |  |
| `environment` | string | no |  |
| `expandMetadata` | string | no |  |
| `fields` | string | no |  |
| `filter` | string | no |  |
| `fromStartTime` | string | no |  |
| `level` | string | no |  |
| `name` | string | no |  |
| `parentObservationId` | string | no |  |
| `parseIoAsJson` | string | no |  |
| `toStartTime` | string | no |  |
| `traceId` | string | no |  |
| `type` | string | no |  |
| `userId` | string | no |  |
| `version` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookmarked": true,
      "completionStartTime": "2026-05-07T12:00:00.000Z",
      "costDetails": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endTime": "2026-05-07T12:00:00.000Z",
      "environment": "string",
      "id": "string",
      "input": "string",
      "internalModelId": "string",
      "latency": 1,
      "level": "string",
      "metadata": "string",
      "modelId": "string",
      "modelParameters": "string",
      "name": "Ava Chen",
      "output": "string",
      "parentObservationId": "string",
      "projectId": "string",
      "promptId": "string",
      "promptName": "Ava Chen",
      "promptVersion": 1,
      "providedModelName": "Ava Chen",
      "public": true,
      "sessionId": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "statusMessage": "string",
      "timeToFirstToken": 1,
      "totalCost": 1,
      "traceId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usageDetails": {},
      "userId": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookmarked` | boolean |  |
| `completionStartTime` | date |  |
| `costDetails` | object |  |
| `createdAt` | date |  |
| `endTime` | date |  |
| `environment` | string |  |
| `id` | string |  |
| `input` | string |  |
| `internalModelId` | string |  |
| `latency` | number |  |
| `level` | string |  |
| `metadata` | string |  |
| `modelId` | string |  |
| `modelParameters` | string |  |
| `name` | string |  |
| `output` | string |  |
| `parentObservationId` | string |  |
| `projectId` | string |  |
| `promptId` | string |  |
| `promptName` | string |  |
| `promptVersion` | number |  |
| `providedModelName` | string |  |
| `public` | boolean |  |
| `sessionId` | string |  |
| `startTime` | date |  |
| `statusMessage` | string |  |
| `timeToFirstToken` | number |  |
| `totalCost` | number |  |
| `traceId` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `usageDetails` | object |  |
| `userId` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Langfuse API, this operation is `GET /v2/observations` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-observations.md) for the provider-specific parameters and requirements.

