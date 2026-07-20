# TxtSync: Add Contact Tags

Adds tags to a contact in TxtSync.

```
POST https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/add-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/add-contact-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "tagIds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/add-contact-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "tagIds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Contact identifier. |
| `tagIds` | list<number> | yes | Tag identifiers to associate to the contact. Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TxtSync API returns.

## Native endpoint

Through the native TxtSync API, this operation is `POST /contacts/:id/tags` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-tags.md) for the provider-specific parameters and requirements.

