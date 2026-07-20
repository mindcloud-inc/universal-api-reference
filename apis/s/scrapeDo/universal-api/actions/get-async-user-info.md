# Scrape do: Get async user info

Retrieves async user information from Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-user-info?${params}`, {
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
      "ActiveJobs": 1,
      "AvaliableCredits": 1,
      "FreeConcurrency": 1,
      "TotalConcurrency": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActiveJobs` | number | Number of active jobs. |
| `AvaliableCredits` | number | Remaining credits. |
| `FreeConcurrency` | number | Available async concurrency. |
| `TotalConcurrency` | number | Total async concurrency. |

## Native endpoint

Through the native Scrape do API, this operation is `GET https://q.scrape.do/api/v1/me` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-user-info.md) for the provider-specific parameters and requirements.

