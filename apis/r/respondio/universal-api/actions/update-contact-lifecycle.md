# respond.io: Update Contact Lifecycle

Updates a contact lifecycle in respond.io.

```
PUT https://connect.mindcloud.co/v1/universal/respondio/latest/actions/update-contact-lifecycle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/update-contact-lifecycle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/update-contact-lifecycle', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Contact identifier (id:, email:, or phone:). |
| `name` | string | yes | Lifecycle name to apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |

## Native endpoint

Through the native respond.io API, this operation is `POST /contact/:identifier/lifecycle/update` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-lifecycle.md) for the provider-specific parameters and requirements.

