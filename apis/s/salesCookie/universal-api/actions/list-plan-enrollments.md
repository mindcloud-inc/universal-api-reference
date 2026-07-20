# Sales Cookie: List Plan Enrollments

Retrieves plan enrollments from Sales Cookie.

```
GET https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-plan-enrollments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-plan-enrollments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-plan-enrollments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sales Cookie API returns.

## Native endpoint

Through the native Sales Cookie API, this operation is `GET /odata/:apiKey/PlanEnrollment` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-plan-enrollments.md) for the provider-specific parameters and requirements.

