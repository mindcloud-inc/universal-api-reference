# ProvenExpert: List Child Rating Summaries

Lists child profile rating summaries in ProvenExpert.

```
GET https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-rating-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-rating-summaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-rating-summaries?${params}`, {
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
      "email": "ava@example.com",
      "ratingValue": 1,
      "reviewCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address for the child profile. |
| `ratingValue` | number | Overall rating for the child profile. |
| `reviewCount` | number | Number of ratings for the child profile. |

## Native endpoint

Through the native ProvenExpert API, this operation is `GET /rating/summary/children` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-child-rating-summaries.md) for the provider-specific parameters and requirements.

