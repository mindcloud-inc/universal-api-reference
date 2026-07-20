# OfficeClip: List Time Offs

Retrieves time off entries from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-time-offs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-time-offs?connectionId=$CONNECTION_ID&limit=25&offset=0&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "category": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-time-offs?${params}`, {
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
| `category` | string | yes | Required OfficeClip category such as mylist, inbox, or archived. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OfficeClip API returns.

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/timeoff-summary` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-offs.md) for the provider-specific parameters and requirements.

