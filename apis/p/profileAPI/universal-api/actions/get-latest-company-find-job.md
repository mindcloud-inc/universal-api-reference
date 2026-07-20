# profileAPI: Get Latest Company Find Job

Retrieves the latest company search job from profileAPI.

```
GET https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/get-latest-company-find-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a profileAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/get-latest-company-find-job?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/get-latest-company-find-job?${params}`, {
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
      "error": {
        "code": 1,
        "message": "string"
      },
      "jobId": "string",
      "progress": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number |  |
| `error.message` | string |  |
| `jobId` | string |  |
| `progress` | number |  |
| `status` | string |  |

## Native endpoint

Through the native profileAPI API, this operation is `GET /companies/find/jobs/latest` (base URL `https://api.profileapi.com/2024-03-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-company-find-job.md) for the provider-specific parameters and requirements.

