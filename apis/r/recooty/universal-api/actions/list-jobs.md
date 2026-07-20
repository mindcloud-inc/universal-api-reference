# Recooty: List Jobs



```
GET https://connect.mindcloud.co/v1/universal/recooty/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recooty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recooty/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recooty/latest/actions/list-jobs?${params}`, {
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
      "company": "string",
      "job_count": 1,
      "jobs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Company name returned by Recooty. |
| `job_count` | number | Total number of published jobs in the response. |
| `jobs` | array<object> | Published jobs returned by the Job Listing API. |

## Native endpoint

Through the native Recooty API, this operation is `GET /v1/jobs/{{credentials.jobListingKey}}` (base URL `https://standaloneapi.recooty.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

