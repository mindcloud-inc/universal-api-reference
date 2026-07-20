# Intervals.icu: Get Athlete Power vs Heart Rate Curve

Retrieves power versus heart rate curves from Intervals.icu.

```
GET https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/get-athlete-power-vs-heart-rate-curve
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intervals.icu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/get-athlete-power-vs-heart-rate-curve?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/get-athlete-power-vs-heart-rate-curve?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Intervals.icu API returns.

## Native endpoint

Through the native Intervals.icu API, this operation is `GET /api/v1/athlete/:id/power-hr-curve` (base URL `https://intervals.icu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-athlete-power-vs-heart-rate-curve.md) for the provider-specific parameters and requirements.

