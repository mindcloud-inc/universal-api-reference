# HubSpot: Get Pipeline Stage by ID

Retrieves a pipeline stage from HubSpot by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-pipeline-stage-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-pipeline-stage-by-id?connectionId=$CONNECTION_ID&objectType=tickets&pipelineId=default&stageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectType": "tickets",
  "pipelineId": "default",
  "stageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-pipeline-stage-by-id?${params}`, {
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
| `objectType` | string | yes | The object type whose pipeline stage to retrieve, such as deals or tickets. Example: `tickets`. |
| `pipelineId` | string | yes | The ID of the pipeline that contains the stage. Example: `default`. |
| `stageId` | string | yes | The ID of the pipeline stage to retrieve. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayOrder": 1,
      "id": "string",
      "label": "string",
      "metadata": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "writePermissions": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `displayOrder` | number |  |
| `id` | string |  |
| `label` | string |  |
| `metadata` | object |  |
| `updatedAt` | date |  |
| `writePermissions` | string |  |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/pipelines/:objectType/:pipelineId/stages/:stageId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline-stage-by-id.md) for the provider-specific parameters and requirements.

