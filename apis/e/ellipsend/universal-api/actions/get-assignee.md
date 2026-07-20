# Ellipsend: Get Assignee

Retrieves an assignee from Ellipsend by ID.

```
GET https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/get-assignee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ellipsend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/get-assignee?connectionId=$CONNECTION_ID&assigneeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assigneeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/get-assignee?${params}`, {
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
| `assigneeId` | number | yes | The assignee ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ellipsend API returns.

## Native endpoint

Through the native Ellipsend API, this operation is `GET /assignee/[:assignee_id]` (base URL `https://api.ellipsend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-assignee.md) for the provider-specific parameters and requirements.

