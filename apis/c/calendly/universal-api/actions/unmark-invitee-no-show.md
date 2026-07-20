# Calendly: Unmark Invitee No Show

Removes a no-show mark from a Calendly invitee.

```
DELETE https://connect.mindcloud.co/v1/universal/calendly/latest/actions/unmark-invitee-no-show
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/unmark-invitee-no-show?connectionId=$CONNECTION_ID&invitee_no_show_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invitee_no_show_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/unmark-invitee-no-show?${params}`, {
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
| `invitee_no_show_uuid` | string | yes | Invitee no-show UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Calendly API returns.

## Native endpoint

Through the native Calendly API, this operation is `DELETE /invitee_no_shows/:invitee_no_show_uuid` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unmark-invitee-no-show.md) for the provider-specific parameters and requirements.

