# Datarobot: List Dataset Versions

Retrieves versions for a dataset from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-dataset-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-dataset-versions?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-dataset-versions?${params}`, {
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
| `datasetId` | string | yes | The ID of the dataset. |

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
      "isDataEngineEligible": true,
      "isLatestVersion": true,
      "isSnapshot": true,
      "name": "Ava Chen",
      "processingState": "string",
      "rowCount": 1,
      "sampleSize": 1,
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
| `isDataEngineEligible` | boolean |  |
| `isLatestVersion` | boolean |  |
| `isSnapshot` | boolean |  |
| `name` | string |  |
| `processingState` | string |  |
| `rowCount` | number |  |
| `sampleSize` | number |  |
| `versionId` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /datasets/:datasetId/versions/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dataset-versions.md) for the provider-specific parameters and requirements.

