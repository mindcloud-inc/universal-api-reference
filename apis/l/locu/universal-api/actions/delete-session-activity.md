# Locu: Delete Session Activity

Deletes an existing session activity from Locu.

```
DELETE https://connect.mindcloud.co/v1/universal/locu/latest/actions/delete-session-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/locu/latest/actions/delete-session-activity?connectionId=$CONNECTION_ID&id=string&activityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "activityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/delete-session-activity?${params}`, {
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
| `id` | string | yes | Session ID that owns the activity. |
| `activityId` | string | yes | Activity ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Locu API, this operation is `DELETE /sessions/:id/activities/:activityId` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-session-activity.md) for the provider-specific parameters and requirements.

