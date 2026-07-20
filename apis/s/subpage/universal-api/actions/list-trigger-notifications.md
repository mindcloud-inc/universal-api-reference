# Subpage: List Trigger Notifications



```
GET https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-trigger-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Subpage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-trigger-notifications?connectionId=$CONNECTION_ID&event=new_lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event": "new_lead"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-trigger-notifications?${params}`, {
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
| `event` | string | yes | Subpage event type to list notifications for, such as new_lead or new_article. Example: `new_lead`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Subpage API returns.

## Native endpoint

Through the native Subpage API, this operation is `GET /call/api/zapier/listtrigger` (base URL `https://editor.subpage.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trigger-notifications.md) for the provider-specific parameters and requirements.

