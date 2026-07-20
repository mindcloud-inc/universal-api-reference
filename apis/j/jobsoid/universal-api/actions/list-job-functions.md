# Jobsoid: List job functions

Retrieves job functions from Jobsoid.

```
GET https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/list-job-functions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobsoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/list-job-functions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/list-job-functions?${params}`, {
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
      "id": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Jobsoid API, this operation is `GET /api/v1/functions` (base URL `https://demo.jobsoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-functions.md) for the provider-specific parameters and requirements.

