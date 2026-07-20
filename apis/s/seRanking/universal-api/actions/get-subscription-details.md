# SE Ranking Data: Get Subscription Details

Retrieves subscription details from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-subscription-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-subscription-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-subscription-details?${params}`, {
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
      "subscriptionInfo": {
        "expiratonDate": "string",
        "startDate": "string",
        "status": "string",
        "unitsLeft": "string",
        "unitsLimit": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriptionInfo` | object |  |
| `subscriptionInfo.expiratonDate` | string |  |
| `subscriptionInfo.startDate` | string |  |
| `subscriptionInfo.status` | string |  |
| `subscriptionInfo.unitsLeft` | string |  |
| `subscriptionInfo.unitsLimit` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /account/subscription` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-details.md) for the provider-specific parameters and requirements.

