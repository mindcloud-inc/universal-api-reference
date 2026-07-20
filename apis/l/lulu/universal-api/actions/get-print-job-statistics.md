# Lulu: Get Print Job Statistics

Retrieves print job statistics from Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-statistics?${params}`, {
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
      "created": 1,
      "error": 1,
      "inProduction": 1,
      "rejected": 1,
      "shipped": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `error` | number |  |
| `inProduction` | number |  |
| `rejected` | number |  |
| `shipped` | number |  |

## Native endpoint

Through the native Lulu API, this operation is `GET /print-jobs/statistics/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-print-job-statistics.md) for the provider-specific parameters and requirements.

