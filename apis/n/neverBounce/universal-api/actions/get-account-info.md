# NeverBounce: Get Account Info

Retrieves account details and usage information from NeverBounce.

```
GET https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-account-info?${params}`, {
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
      "creditsInfo": {
        "freeCreditsRemaining": 1,
        "freeCreditsUsed": 1,
        "paidCreditsRemaining": 1,
        "paidCreditsUsed": 1
      },
      "executionTime": 1,
      "jobCounts": {
        "completed": 1,
        "processing": 1,
        "queued": 1,
        "underReview": 1
      },
      "status": "string",
      "subscriptionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsInfo` | object |  |
| `creditsInfo.freeCreditsRemaining` | number |  |
| `creditsInfo.freeCreditsUsed` | number |  |
| `creditsInfo.paidCreditsRemaining` | number |  |
| `creditsInfo.paidCreditsUsed` | number |  |
| `executionTime` | number |  |
| `jobCounts` | object |  |
| `jobCounts.completed` | number |  |
| `jobCounts.processing` | number |  |
| `jobCounts.queued` | number |  |
| `jobCounts.underReview` | number |  |
| `status` | string |  |
| `subscriptionType` | string |  |

## Native endpoint

Through the native NeverBounce API, this operation is `GET /account/info` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

