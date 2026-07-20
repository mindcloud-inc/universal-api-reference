# Datarobot: List Datasets

Retrieves a list of datasets from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-datasets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Datarobot API, this operation is `GET /datasets/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-datasets.md) for the provider-specific parameters and requirements.

