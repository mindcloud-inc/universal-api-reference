# Jetbuilt: Update Client Contact

Update a specified contact for a specified client.

```
PUT https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/update-client-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/update-client-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/update-client-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client_id` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `title` | string | no |  |
| `emailAddress` | string | no |  |
| `phoneNumber1` | string | no |  |
| `phoneNumber2` | string | no |  |
| `description` | string | no |  |
| `primary` | boolean | no |  |
| `contact_id` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jetbuilt API returns.

## Native endpoint

Through the native Jetbuilt API, this operation is `PATCH clients/:client_id/contacts/:contact_id` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client-contact.md) for the provider-specific parameters and requirements.

