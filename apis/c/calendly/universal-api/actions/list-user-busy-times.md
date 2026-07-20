# Calendly: List User Busy Times

Retrieves user busy times from Calendly.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-user-busy-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-user-busy-times?connectionId=$CONNECTION_ID&user=https%3A%2F%2Fapi.calendly.com%2Fusers%2F264e5a40-147f-45f9-a96c-a6f2f0a91dff&startTime=2026-02-26T00%3A00%3A00Z&endTime=2026-03-05T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user": "https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff",
  "startTime": "2026-02-26T00:00:00Z",
  "endTime": "2026-03-05T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-user-busy-times?${params}`, {
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
| `user` | list | yes | User URI filter. One of: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. Default: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |
| `startTime` | date | yes | Start of interval (ISO-8601). Default: `2026-02-26T00:00:00Z`. |
| `endTime` | date | yes | End of interval (ISO-8601). Default: `2026-03-05T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> | User busy-time intervals. |

## Native endpoint

Through the native Calendly API, this operation is `GET /user_busy_times` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-busy-times.md) for the provider-specific parameters and requirements.

