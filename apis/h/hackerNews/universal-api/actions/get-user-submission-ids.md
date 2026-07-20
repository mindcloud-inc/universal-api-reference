# Hacker News: Get User Submission IDs

Retrieves a user's submission IDs from Hacker News.

```
GET https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-user-submission-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hacker News `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-user-submission-ids?connectionId=$CONNECTION_ID&id=pg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "pg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-user-submission-ids?${params}`, {
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
| `id` | string | yes | Hacker News username. Default: `pg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array<number> | Ordered submitted item IDs for a user. |

## Native endpoint

Through the native Hacker News API, this operation is `GET /user/:id/submitted.json` (base URL `https://hacker-news.firebaseio.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-submission-ids.md) for the provider-specific parameters and requirements.

