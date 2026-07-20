# MessageBird: Get Channel Details for a Contact



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel-details-for-a-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel-details-for-a-contact?connectionId=$CONNECTION_ID&workspaceId=string&channelId=string&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "channelId": "string",
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel-details-for-a-contact?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | The Bird workspace ID that owns the channel. |
| `channelId` | string | yes | The Bird channel ID to inspect. |
| `contactId` | string | yes | The Bird contact ID to inspect for channel details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isPermanentSession": true,
      "metadata": {},
      "serviceWindowExpireAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isPermanentSession` | boolean |  |
| `metadata` | object |  |
| `serviceWindowExpireAt` | date |  |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/channels/:channelId/contacts/:contactId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-details-for-a-contact.md) for the provider-specific parameters and requirements.

