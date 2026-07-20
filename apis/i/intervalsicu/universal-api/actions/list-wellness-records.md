# Intervals.icu: List Wellness Records

Retrieves wellness records from Intervals.icu.

```
GET https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/list-wellness-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intervals.icu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/list-wellness-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/list-wellness-records?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Intervals.icu API returns.

## Native endpoint

Through the native Intervals.icu API, this operation is `GET /api/v1/athlete/:id/wellness:ext` (base URL `https://intervals.icu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-wellness-records.md) for the provider-specific parameters and requirements.

