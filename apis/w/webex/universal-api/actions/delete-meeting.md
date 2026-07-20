# Webex: Delete Meeting

Deletes an existing meeting from Webex.

```
DELETE https://connect.mindcloud.co/v1/universal/webex/latest/actions/delete-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webex/latest/actions/delete-meeting?connectionId=$CONNECTION_ID&meetingId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/delete-meeting?${params}`, {
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
| `meetingId` | string | yes | Meeting identifier. Example: `123456789`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Webex API returns.

## Native endpoint

Through the native Webex API, this operation is `DELETE /meetings/:meetingId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-meeting.md) for the provider-specific parameters and requirements.

