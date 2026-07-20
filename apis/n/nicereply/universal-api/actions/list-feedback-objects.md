# Nicereply: List Feedback Objects

Retrieves a list of feedback objects from Nicereply.

```
GET https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/list-feedback-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nicereply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/list-feedback-objects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/list-feedback-objects?${params}`, {
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
| `sortOrder` | string | no | Sort feedback objects by created_at using asc or desc. Default: `desc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nicereply API returns.

## Native endpoint

Through the native Nicereply API, this operation is `GET /feedback-objects` (base URL `https://api.nicereply.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-feedback-objects.md) for the provider-specific parameters and requirements.

