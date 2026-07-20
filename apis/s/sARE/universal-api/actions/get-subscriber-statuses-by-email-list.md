# SARE: Get Subscriber Statuses By Email List

Retrieves subscriber statuses from SARE by email address list.

```
GET https://connect.mindcloud.co/v1/universal/sARE/latest/actions/get-subscriber-statuses-by-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SARE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/get-subscriber-statuses-by-email-list?connectionId=$CONNECTION_ID&emails%5B%5D=%5Bobject%20Object%5D&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails[]": "[object Object]",
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sARE/latest/actions/get-subscriber-statuses-by-email-list?${params}`, {
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
| `emails[]` | array<object> | yes | Array of email lookup objects for the SARE status route. |
| `page` | number | yes | Zero-based page number for the SARE route. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SARE API returns.

## Native endpoint

Through the native SARE API, this operation is `POST /email/status_by_email_list/:page` (base URL `https://s.enewsletter.pl/api/v1/{{credentials.uid}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-statuses-by-email-list.md) for the provider-specific parameters and requirements.

