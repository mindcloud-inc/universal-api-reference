# ProvenExpert: Get Rating Summary

Retrieves your profile rating summary from ProvenExpert.

```
GET https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-rating-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-rating-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-rating-summary?${params}`, {
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
      "ratingValue": 1,
      "recommendationRate": 1,
      "reviewCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ratingValue` | number | Average rating value returned by ProvenExpert. |
| `recommendationRate` | number | Recommendation rate returned by the summary endpoint. |
| `reviewCount` | number | Number of reviews included in the summary. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /rating/summary/get` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rating-summary.md) for the provider-specific parameters and requirements.

