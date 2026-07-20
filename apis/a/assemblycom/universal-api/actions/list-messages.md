# Assembly.com: List Messages

Retrieves messages from an Assembly.com message channel.

```
GET https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-messages?${params}`, {
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
| `channelId` | string | yes | The Message Channel to retrieve messages from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "channelId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "identityId": "string",
          "isAttachmentIncluded": true,
          "object": "string",
          "senderId": "string",
          "text": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].channelId` | string |  |
| `data[].createdAt` | date |  |
| `data[].id` | string |  |
| `data[].identityId` | string |  |
| `data[].isAttachmentIncluded` | boolean |  |
| `data[].object` | string |  |
| `data[].senderId` | string |  |
| `data[].text` | string |  |
| `data[].updatedAt` | date |  |

## Native endpoint

Through the native Assembly.com API, this operation is `GET /messages` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

