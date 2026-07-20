# CalendarHero: Get Directory

Retrieves a directory from CalendarHero.

```
GET https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-directory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-directory?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CalendarHero API returns.

## Native endpoint

Through the native CalendarHero API, this operation is `GET /user/directories/{uuid}` (base URL `https://api.calendarhero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-directory.md) for the provider-specific parameters and requirements.

