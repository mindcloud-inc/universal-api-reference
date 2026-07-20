# Mailchimp: Update Member Tags

Updates tags for a member in a Mailchimp audience.

```
PUT https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-member-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-member-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "string",
  "subscriber_hash": "string",
  "tags[]": [
    {}
  ],
  "tags[].name": "Ava Chen",
  "tags[].status": "active"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-member-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": "string",
    "subscriber_hash": "string",
    "tags[]": [{}],
    "tags[].name": "Ava Chen",
    "tags[].status": "active"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `is_syncing` | boolean | no | Whether tag updates should sync. |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `subscriber_hash` | string | yes | MD5 hash of the lowercase subscriber email address. |
| `tags[]` | array<object> | yes | Tag updates array. |
| `tags[].name` | string | yes | The merge tag name. |
| `tags[].status` | list<string> | yes | Whether the tag should be active or inactive. One of: `active`, `inactive`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mailchimp API returns.

## Native endpoint

Through the native Mailchimp API, this operation is `POST lists/:list_id/members/:subscriber_hash/tags` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member-tags.md) for the provider-specific parameters and requirements.

