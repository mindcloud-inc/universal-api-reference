# Datarobot: Get Use Case Dataset

Retrieves dataset details for a use case from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-use-case-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-use-case-dataset?connectionId=$CONNECTION_ID&datasetId=string&useCaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string",
  "useCaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-use-case-dataset?${params}`, {
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
| `datasetId` | string | yes |  |
| `useCaseId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        "string"
      ],
      "columnCount": 1,
      "createdBy": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "dataPersisted": true,
      "datasetId": "string",
      "datasetSize": 1,
      "dataSourceType": "string",
      "description": "string",
      "featureCount": 1,
      "isDataEngineEligible": true,
      "isLatestVersion": true,
      "isSnapshot": true,
      "name": "Ava Chen",
      "processingState": "string",
      "rowCount": 1,
      "uri": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<string> |  |
| `columnCount` | number |  |
| `createdBy` | string |  |
| `creationDate` | date |  |
| `dataPersisted` | boolean |  |
| `datasetId` | string |  |
| `datasetSize` | number |  |
| `dataSourceType` | string |  |
| `description` | string |  |
| `featureCount` | number |  |
| `isDataEngineEligible` | boolean |  |
| `isLatestVersion` | boolean |  |
| `isSnapshot` | boolean |  |
| `name` | string |  |
| `processingState` | string |  |
| `rowCount` | number |  |
| `uri` | string |  |
| `versionId` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /useCases/:useCaseId/datasets/:datasetId/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-use-case-dataset.md) for the provider-specific parameters and requirements.

