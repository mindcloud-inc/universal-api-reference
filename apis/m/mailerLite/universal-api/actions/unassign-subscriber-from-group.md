# MailerLite: Unassign Subscriber from Group

Removes a subscriber from a group in MailerLite.

```
DELETE https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/unassign-subscriber-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/unassign-subscriber-from-group?connectionId=$CONNECTION_ID&subscriber_id=180863157267334516&group_id=180900000000000001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriber_id": "180863157267334516",
  "group_id": "180900000000000001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/unassign-subscriber-from-group?${params}`, {
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
| `subscriber_id` | string | yes | Existing MailerLite subscriber identifier. Example: `180863157267334516`. |
| `group_id` | string | yes | Existing MailerLite group identifier. Example: `180900000000000001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body returned when the subscriber is removed from the group successfully. |

## Native endpoint

Through the native MailerLite API, this operation is `DELETE /subscribers/:subscriber_id/groups/:group_id` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unassign-subscriber-from-group.md) for the provider-specific parameters and requirements.

