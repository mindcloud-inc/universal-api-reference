# Datarobot: List Use Case Datasets

Retrieves datasets for a use case from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-case-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-case-datasets?connectionId=$CONNECTION_ID&useCaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "useCaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-case-datasets?${params}`, {
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
| `useCaseId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataPersisted": true,
      "datasetId": "string",
      "datasetSize": 1,
      "datasetSourceType": "string",
      "dataSourceType": "string",
      "dataType": "string",
      "description": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "processingState": "string",
      "rowCount": 1,
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnCount` | number |  |
| `createdAt` | date |  |
| `dataPersisted` | boolean |  |
| `datasetId` | string |  |
| `datasetSize` | number |  |
| `datasetSourceType` | string |  |
| `dataSourceType` | string |  |
| `dataType` | string |  |
| `description` | string |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `processingState` | string |  |
| `rowCount` | number |  |
| `versionId` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /useCases/:useCaseId/datasets/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-use-case-datasets.md) for the provider-specific parameters and requirements.

