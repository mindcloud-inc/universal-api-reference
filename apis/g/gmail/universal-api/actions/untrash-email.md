# Google Mail: Untrash Email

Removes a Gmail message from trash.

```
PUT https://connect.mindcloud.co/v1/universal/gmail/latest/actions/untrash-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/untrash-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "17c7f5f9f1d6c1a2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gmail/latest/actions/untrash-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "17c7f5f9f1d6c1a2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Gmail message ID to restore from trash. Example: `17c7f5f9f1d6c1a2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "labelIds": [
        "string"
      ],
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `labelIds[]` | string |  |
| `threadId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `POST /messages/:id/untrash` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/untrash-email.md) for the provider-specific parameters and requirements.

