# Growby: Bulk Add Contacts To Group By Group Name

Adds multiple contacts to a Growby group by group name.

```
POST https://connect.mindcloud.co/v1/universal/growby/latest/actions/bulk-add-contacts-to-group-by-group-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growby/latest/actions/bulk-add-contacts-to-group-by-group-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupname": "Ava Chen",
  "contactList": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growby/latest/actions/bulk-add-contacts-to-group-by-group-name', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupname": "Ava Chen",
    "contactList": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupname` | string | yes | Exact Growby group name. |
| `contactList` | string | yes | Comma-separated list of Growby contact ids. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Growby API returns.

## Native endpoint

Through the native Growby API, this operation is `POST /groups/:groupname/contacts/:contactlist` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-add-contacts-to-group-by-group-name.md) for the provider-specific parameters and requirements.

