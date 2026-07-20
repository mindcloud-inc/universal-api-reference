# Growby: Add Contact To Group By Group Name

Adds a contact to a Growby group by group name.

```
POST https://connect.mindcloud.co/v1/universal/growby/latest/actions/add-contact-to-group-by-group-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growby/latest/actions/add-contact-to-group-by-group-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupname": "Ava Chen",
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growby/latest/actions/add-contact-to-group-by-group-name', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupname": "Ava Chen",
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupname` | string | yes | Exact Growby group name. |
| `contactId` | number | yes | Numeric Growby contact id to add to the group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Growby API returns.

## Native endpoint

Through the native Growby API, this operation is `POST /groups/:groupname/contacts/:contactId` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-group-by-group-name.md) for the provider-specific parameters and requirements.

