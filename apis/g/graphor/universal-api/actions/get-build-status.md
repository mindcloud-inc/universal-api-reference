# Graphor: Get Build Status

Retrieves source build status from Graphor by build ID.

```
GET https://connect.mindcloud.co/v1/universal/graphor/latest/actions/get-build-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/get-build-status?connectionId=$CONNECTION_ID&buildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "buildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphor/latest/actions/get-build-status?${params}`, {
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
| `buildId` | string | yes | The build identifier returned by an ingestion or reprocess request. |
| `page` | string | no | 1-based page number for paginated build elements. |
| `pageSize` | string | no | Number of build elements to return per page when pagination is used. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buildId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "fileId": "string",
      "fileName": "Ava Chen",
      "message": "string",
      "method": "string",
      "status": "string",
      "success": true,
      "totalPages": 1,
      "totalPartitions": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buildId` | string |  |
| `createdAt` | date |  |
| `error` | string |  |
| `fileId` | string |  |
| `fileName` | string |  |
| `message` | string |  |
| `method` | string |  |
| `status` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalPartitions` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Graphor API, this operation is `GET /builds/{buildId}` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-build-status.md) for the provider-specific parameters and requirements.

