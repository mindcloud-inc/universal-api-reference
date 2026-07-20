# Communi App: List Messages



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-messages?connectionId=$CONNECTION_ID&conversation=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversation": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-messages?${params}`, {
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
| `conversation` | number | yes | Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "contentType": 1,
      "conversation": "string",
      "createdBy": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "creationRandom": "string",
      "id": 1,
      "messageFormatted": "string",
      "replyTo": "string",
      "serialId": 1,
      "type": 1,
      "updatedBy": 1,
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_loadStatus` | number |  |
| `_rls` | number |  |
| `contentType` | number |  |
| `conversation` | string |  |
| `createdBy` | number |  |
| `createdOn` | date |  |
| `creationRandom` | string |  |
| `id` | number |  |
| `messageFormatted` | string |  |
| `replyTo` | string |  |
| `serialId` | number |  |
| `type` | number |  |
| `updatedBy` | number |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/message` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

