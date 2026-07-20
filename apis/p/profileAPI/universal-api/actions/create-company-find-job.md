# profileAPI: Create Company Find Job

Creates a company search job in profileAPI.

```
POST https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/create-company-find-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a profileAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/create-company-find-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filters": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/create-company-find-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filters": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | yes | Filter groups containing all/any filter arrays for the company find job. Example: `[object Object]`. |
| `limit` | number | no | Maximum number of matching companies for the background job when supported by provider filters. Default: `10`. Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "jobUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `jobUrl` | string |  |

## Native endpoint

Through the native profileAPI API, this operation is `POST /companies/find/jobs` (base URL `https://api.profileapi.com/2024-03-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company-find-job.md) for the provider-specific parameters and requirements.

