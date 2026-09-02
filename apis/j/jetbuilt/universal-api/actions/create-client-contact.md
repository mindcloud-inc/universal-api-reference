# Jetbuilt: Create Client Contact



```
POST https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-client-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-client-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-client-contact', {
  method: 'POST',
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jetbuilt API returns.

## Native endpoint

Through the native Jetbuilt API, this operation is `POST clients/:client_id/contacts` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-contact.md) for the provider-specific parameters and requirements.

