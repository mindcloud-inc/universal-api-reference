# HubSpot: Create Pipeline Stage



```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-pipeline-stage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-pipeline-stage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectType": "deals",
  "pipelineId": "default",
  "label": "Contract signed",
  "displayOrder": "4",
  "metadata.probability": "0.8"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-pipeline-stage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectType": "deals",
    "pipelineId": "default",
    "label": "Contract signed",
    "displayOrder": "4",
    "metadata.probability": "0.8"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectType` | string | yes | The CRM object type whose pipeline will receive the new stage. Use `deals` for deal stages. Example: `deals`. |
| `pipelineId` | string | yes | The ID of the pipeline that should receive the new stage. Example: `default`. |
| `label` | string | yes | The name of the stage as it is displayed in HubSpot. The label must be unique within the pipeline. Example: `Contract signed`. |
| `displayOrder` | number | yes | The order of the stage in the pipeline. If multiple stages share the same order, HubSpot sorts them alphabetically by label. Example: `4`. |
| `metadata.probability` | string | yes | For deal stages, the required close probability from `0.0` to `1.0`, where `0.0` is Closed Lost and `1.0` is Closed Won. Example: `0.8`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Additional stage metadata. For deal stages, HubSpot requires `probability` inside this object. |

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
| `archived` | boolean | Whether the stage is archived. |
| `createdAt` | date | When the stage was created. |
| `displayOrder` | number | The order of the stage in the pipeline. |
| `id` | string | The unique ID of the created pipeline stage. |
| `label` | string | The stage name displayed in HubSpot. |
| `metadata` | object | Stage metadata such as deal probability. |
| `updatedAt` | date | When the stage was last updated. |
| `writePermissions` | string | HubSpot write-permission mode for the stage. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/pipelines/:objectType/:pipelineId/stages` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pipeline-stage.md) for the provider-specific parameters and requirements.

