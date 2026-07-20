# Google Mail: Update Label

Updates a Gmail label.

```
PUT https://connect.mindcloud.co/v1/universal/gmail/latest/actions/update-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/update-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "Label_1234567890"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gmail/latest/actions/update-label', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "Label_1234567890"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Label ID to update. Example: `Label_1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `PUT /labels/:id` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-label.md) for the provider-specific parameters and requirements.

