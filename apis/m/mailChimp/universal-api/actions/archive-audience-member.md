# Mailchimp: Archive Audience Member

Archives a member in a Mailchimp audience.

```
DELETE https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/archive-audience-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/archive-audience-member?connectionId=$CONNECTION_ID&list_id=string&subscriber_hash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "string",
  "subscriber_hash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/archive-audience-member?${params}`, {
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
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `subscriber_hash` | string | yes | MD5 hash of the lowercase subscriber email address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mailchimp API returns.

## Native endpoint

Through the native Mailchimp API, this operation is `DELETE lists/:list_id/members/:subscriber_hash` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-audience-member.md) for the provider-specific parameters and requirements.

