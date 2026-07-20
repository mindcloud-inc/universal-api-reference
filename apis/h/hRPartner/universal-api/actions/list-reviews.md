# HR Partner: List Reviews



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-reviews?${params}`, {
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
      "comments": "string",
      "description": "string",
      "employee": {},
      "id": 1,
      "reviewDate": "2026-05-07T12:00:00.000Z",
      "reviewer": "string",
      "reviewStatus": "string",
      "reviewType": "string",
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `description` | string |  |
| `employee` | object |  |
| `id` | number |  |
| `reviewDate` | date |  |
| `reviewer` | string |  |
| `reviewStatus` | string |  |
| `reviewType` | string |  |
| `score` | number |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /reviews` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

