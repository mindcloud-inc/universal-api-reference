# MailSlurp Email Plugin: List Webhooks

Retrieves webhooks from your MailSlurp account.

```
GET https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {
          "createdAt": "string",
          "eventName": "Ava Chen",
          "healthStatus": "string",
          "id": "string",
          "inboxId": "string",
          "url": "https://example.com"
        }
      ],
      "number": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[].createdAt` | string |  |
| `content[].eventName` | string |  |
| `content[].healthStatus` | string |  |
| `content[].id` | string |  |
| `content[].inboxId` | string |  |
| `content[].url` | string |  |
| `number` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `GET /webhooks/paginated` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

