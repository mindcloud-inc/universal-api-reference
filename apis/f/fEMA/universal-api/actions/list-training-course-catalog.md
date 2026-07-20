# FEMA: List Training Course Catalog

Retrieves FEMA training course catalog entries.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-training-course-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-training-course-catalog?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-training-course-catalog?${params}`, {
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
      "courseAcronym": "string",
      "courseActive": true,
      "courseCatalogNumber": "string",
      "courseCEUType": "string",
      "courseContactHours": 1,
      "courseContinuingEdCredits": "string",
      "courseDeliveryMethods": "string",
      "courseDescription": "string",
      "courseDurationDays": 1,
      "courseDurationHours": 1,
      "courseID": "string",
      "courseLevel": "string",
      "courseRequiredPrereqs": "string",
      "courseTitle": "string",
      "courseTrainingProviders": "string",
      "courseVersion": "string",
      "dataSource": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `courseAcronym` | string |  |
| `courseActive` | boolean |  |
| `courseCatalogNumber` | string |  |
| `courseCEUType` | string |  |
| `courseContactHours` | number |  |
| `courseContinuingEdCredits` | string |  |
| `courseDeliveryMethods` | string |  |
| `courseDescription` | string |  |
| `courseDurationDays` | number |  |
| `courseDurationHours` | number |  |
| `courseID` | string |  |
| `courseLevel` | string |  |
| `courseRequiredPrereqs` | string |  |
| `courseTitle` | string |  |
| `courseTrainingProviders` | string |  |
| `courseVersion` | string |  |
| `dataSource` | string |  |
| `id` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/TrainingCourseCatalog` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-training-course-catalog.md) for the provider-specific parameters and requirements.

