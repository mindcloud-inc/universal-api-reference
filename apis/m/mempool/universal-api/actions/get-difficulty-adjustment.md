# Mempool: Get Difficulty Adjustment

Retrieves difficulty adjustment details from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-difficulty-adjustment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-difficulty-adjustment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-difficulty-adjustment?${params}`, {
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
      "adjustedTimeAvg": 1,
      "difficultyChange": 1,
      "estimatedRetargetDate": 1,
      "expectedBlocks": 1,
      "nextRetargetHeight": 1,
      "previousRetarget": 1,
      "previousTime": 1,
      "progressPercent": 1,
      "remainingBlocks": 1,
      "remainingTime": 1,
      "timeAvg": 1,
      "timeOffset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjustedTimeAvg` | number |  |
| `difficultyChange` | number |  |
| `estimatedRetargetDate` | number |  |
| `expectedBlocks` | number |  |
| `nextRetargetHeight` | number |  |
| `previousRetarget` | number |  |
| `previousTime` | number |  |
| `progressPercent` | number |  |
| `remainingBlocks` | number |  |
| `remainingTime` | number |  |
| `timeAvg` | number |  |
| `timeOffset` | number |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /v1/difficulty-adjustment` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-difficulty-adjustment.md) for the provider-specific parameters and requirements.

