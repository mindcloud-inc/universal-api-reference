# THE HILL: List Email Newsletters

Retrieves email newsletters from The Hill.

```
GET https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/list-email-newsletters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a THE HILL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/list-email-newsletters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/list-email-newsletters?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native THE HILL API returns.

## Native endpoint

Through the native THE HILL API, this operation is `GET /wp/v2/email_newsletter` (base URL `https://thehill.com/wp-json/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-email-newsletters.md) for the provider-specific parameters and requirements.

