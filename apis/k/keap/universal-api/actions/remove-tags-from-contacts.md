# Keap: Remove Tags From Contacts



```
PUT https://connect.mindcloud.co/v1/universal/keap/latest/actions/remove-tags-from-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keap/latest/actions/remove-tags-from-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_ids": "string",
  "tag_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keap/latest/actions/remove-tags-from-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_ids": "string",
    "tag_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_ids` | list<string> | yes | Array of contact IDs to remove the tag from. |
| `tag_id` | string | yes | The unique identifier of the tag. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Keap API returns.

## Native endpoint

Through the native Keap API, this operation is `POST /tags/{tag_id}/contacts:removeTags` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tags-from-contacts.md) for the provider-specific parameters and requirements.

