# EZ Texting: Update Contact Group

Updates a contact group in EZ Texting.

```
PUT https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/update-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/update-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/update-contact-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Contact group ID |
| `name` | string | yes | Contact group name |
| `note` | string | no | Contact group note |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EZ Texting API returns.

## Native endpoint

Through the native EZ Texting API, this operation is `PUT /contact-groups/:id` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-group.md) for the provider-specific parameters and requirements.

