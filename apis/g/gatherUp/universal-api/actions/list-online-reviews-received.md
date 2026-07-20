# GatherUp: List Online Reviews Received

Retrieves a list of online reviews from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-online-reviews-received
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-online-reviews-received?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-online-reviews-received?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | number | no | Business id (or multiple comma-separated ids.) |
| `from` | string | no | Received from |
| `page` | number | no | Page Default: `1`. |
| `to` | string | no | Received to |
| `type[]` | array<string> | no | Review type |
| `visible` | number | no | Show reviews which are visible or not |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "count": 1,
      "errorCode": 1,
      "errorMessage": "string",
      "page": 1,
      "pages": 1,
      "perPage": 1,
      "reviewAuthor": "string",
      "reviewContent": "string",
      "reviewGoogleAttributesNegative": "string",
      "reviewGoogleAttributesPositive": "string",
      "reviewId": "string",
      "reviewRating": 1,
      "reviewTime": "string",
      "reviewType": "string",
      "reviewVisible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `count` | number |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `perPage` | number |  |
| `reviewAuthor` | string |  |
| `reviewContent` | string |  |
| `reviewGoogleAttributesNegative` | string |  |
| `reviewGoogleAttributesPositive` | string |  |
| `reviewId` | string |  |
| `reviewRating` | number |  |
| `reviewTime` | string |  |
| `reviewType` | string |  |
| `reviewVisible` | boolean |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /online-reviews/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-online-reviews-received.md) for the provider-specific parameters and requirements.

