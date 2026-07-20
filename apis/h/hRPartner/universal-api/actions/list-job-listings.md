# HR Partner: List Job Listings



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-job-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-job-listings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-job-listings?${params}`, {
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
      "department": "string",
      "employmentStatus": "string",
      "id": "string",
      "isActive": true,
      "location": "string",
      "position": "string",
      "publishAt": "2026-05-07T12:00:00.000Z",
      "responseEmail": "ava@example.com",
      "summary": "string",
      "title": "string",
      "unpublishAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `department` | string |  |
| `employmentStatus` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `location` | string |  |
| `position` | string |  |
| `publishAt` | date |  |
| `responseEmail` | string |  |
| `summary` | string |  |
| `title` | string |  |
| `unpublishAt` | date |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /jobs` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-listings.md) for the provider-specific parameters and requirements.

