# Blueink: Update Person

Updates an existing person in Blueink.

```
PUT https://connect.mindcloud.co/v1/universal/blueink/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "personId": "string",
  "channels[].kind": "string",
  "channels[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueink/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "personId": "string",
    "channels[].kind": "string",
    "channels[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | string | yes | Person ID to update. |
| `name` | string | no | Updated name for the person. |
| `channels[].kind` | string | yes | Contact channel type. Use em for email. |
| `channels[].email` | string | yes | Email address for the contact channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        {
          "email": "ava@example.com",
          "id": "string",
          "kind": "string",
          "phone": "string"
        }
      ],
      "id": "string",
      "isUser": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels[].email` | string |  |
| `channels[].id` | string |  |
| `channels[].kind` | string |  |
| `channels[].phone` | string |  |
| `id` | string |  |
| `isUser` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `PUT /persons/:personId/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

