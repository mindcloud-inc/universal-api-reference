# Beamer: Get Unread Count

Retrieves the unread post count from Beamer.

```
GET https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-unread-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-unread-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-unread-count?${params}`, {
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
| `filter` | string | no | Segment filter used to match posts for the user. |
| `dateFrom` | date | no | Only count posts published on or after this date and time. |
| `userId` | string | no | Unique identifier for the user in your own app. |
| `userFirstName` | string | no | First name to include in the generated feed URL context. |
| `userLastName` | string | no | Last name to include in the generated feed URL context. |
| `userEmail` | string | no | Email address to include in the generated feed URL context. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `GET /v0/unread/count` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-unread-count.md) for the provider-specific parameters and requirements.

