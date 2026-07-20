# Clarifai: Update Dataset Version

Updates an existing dataset version in Clarifai.

```
PATCH https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-dataset-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PATCH "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-dataset-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-dataset-version', {
  method: 'PATCH',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | no | Clarifai app ID. |
| `datasetId` | string | no | Clarifai dataset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datasetVersions": [
        {
          "annotationFilterConfig": {
            "annotationFilter": {
              "appId": "string",
              "createdAt": "string",
              "id": "string",
              "modifiedAt": "string",
              "userId": "string"
            }
          },
          "appId": "string",
          "createdAt": "string",
          "datasetId": "string",
          "description": "string",
          "embedModelVersionIds": [
            "string"
          ],
          "id": "string",
          "metrics": {
            "/": {
              "boundingBoxesCount": "string",
              "embeddingsCount": "string",
              "framesCount": "string",
              "inputsCount": "string",
              "inputsWithGeoCount": "string",
              "inputsWithMetadataCount": "string",
              "masksCount": "string",
              "pointsCount": "string",
              "polygonsCount": "string",
              "positiveFrameTagsCount": "string",
              "positiveInputTagsCount": "string",
              "positiveRegionTagsCount": "string",
              "regionsCount": "string",
              "unlabeledInputsCount": "string"
            }
          },
          "modifiedAt": "string",
          "requestOrigin": 1,
          "status": {
            "code": 1,
            "description": "string",
            "httpStatusCode": 1
          },
          "userId": "string",
          "visibility": {
            "gettable": 1
          }
        }
      ],
      "status": {
        "code": 1,
        "description": "string",
        "httpStatusCode": 1,
        "reqId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasetVersions[].annotationFilterConfig.annotationFilter.appId` | string |  |
| `datasetVersions[].annotationFilterConfig.annotationFilter.createdAt` | string |  |
| `datasetVersions[].annotationFilterConfig.annotationFilter.id` | string |  |
| `datasetVersions[].annotationFilterConfig.annotationFilter.modifiedAt` | string |  |
| `datasetVersions[].annotationFilterConfig.annotationFilter.userId` | string |  |
| `datasetVersions[].appId` | string |  |
| `datasetVersions[].createdAt` | string |  |
| `datasetVersions[].datasetId` | string |  |
| `datasetVersions[].description` | string |  |
| `datasetVersions[].embedModelVersionIds[]` | string |  |
| `datasetVersions[].id` | string |  |
| `datasetVersions[].metrics./.boundingBoxesCount` | string |  |
| `datasetVersions[].metrics./.embeddingsCount` | string |  |
| `datasetVersions[].metrics./.framesCount` | string |  |
| `datasetVersions[].metrics./.inputsCount` | string |  |
| `datasetVersions[].metrics./.inputsWithGeoCount` | string |  |
| `datasetVersions[].metrics./.inputsWithMetadataCount` | string |  |
| `datasetVersions[].metrics./.masksCount` | string |  |
| `datasetVersions[].metrics./.pointsCount` | string |  |
| `datasetVersions[].metrics./.polygonsCount` | string |  |
| `datasetVersions[].metrics./.positiveFrameTagsCount` | string |  |
| `datasetVersions[].metrics./.positiveInputTagsCount` | string |  |
| `datasetVersions[].metrics./.positiveRegionTagsCount` | string |  |
| `datasetVersions[].metrics./.regionsCount` | string |  |
| `datasetVersions[].metrics./.unlabeledInputsCount` | string |  |
| `datasetVersions[].modifiedAt` | string |  |
| `datasetVersions[].requestOrigin` | number |  |
| `datasetVersions[].status.code` | number |  |
| `datasetVersions[].status.description` | string |  |
| `datasetVersions[].status.httpStatusCode` | number |  |
| `datasetVersions[].userId` | string |  |
| `datasetVersions[].visibility.gettable` | number |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.httpStatusCode` | number |  |
| `status.reqId` | string |  |

## Native endpoint

Through the native Clarifai API, this operation is `PATCH /v2/users/{{credentials.userId}}/apps/{{appId}}/datasets/{{datasetId}}/versions` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dataset-version.md) for the provider-specific parameters and requirements.

