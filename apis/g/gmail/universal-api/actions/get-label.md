# Google Mail: Get Label

Retrieves a Gmail label.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-label?connectionId=$CONNECTION_ID&labelId=labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "labelId": "labels"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-label?${params}`, {
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
| `labelId` | string | yes | hidden... Default: `labels`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": {
        "backgroundColor": "string",
        "textColor": "string"
      },
      "id": "string",
      "labelListVisibility": "string",
      "messageListVisibility": "string",
      "messagesTotal": 1,
      "messagesUnread": 1,
      "name": "Ava Chen",
      "threadsTotal": 1,
      "threadsUnread": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color.backgroundColor` | string |  |
| `color.textColor` | string |  |
| `id` | string |  |
| `labelListVisibility` | string |  |
| `messageListVisibility` | string |  |
| `messagesTotal` | number |  |
| `messagesUnread` | number |  |
| `name` | string |  |
| `threadsTotal` | number |  |
| `threadsUnread` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /labels/:labelId` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-label.md) for the provider-specific parameters and requirements.

