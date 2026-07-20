# CalendarHero: Get Savings

Retrieves savings information from CalendarHero.

```
GET https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-savings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-savings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-savings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CalendarHero API returns.

## Native endpoint

Through the native CalendarHero API, this operation is `GET /user/savings` (base URL `https://api.calendarhero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-savings.md) for the provider-specific parameters and requirements.

