# Zoho Desk: List Channels

Retrieve currently installed channels including `System`, `Channel Integration` and `Instant Messaging` channels.

```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-channels?${params}`, {
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
      "acceptsReplies": true,
      "appName": {},
      "code": "string",
      "departmentId": {},
      "externalId": {},
      "mappedIntegration": {},
      "name": "Ava Chen",
      "photoURL": {},
      "replyConfig": {
        "acceptsAttachments": true,
        "contentTypes": [
          "string"
        ],
        "includeQuotedMessage": true,
        "updateRecords": true
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptsReplies` | boolean |  |
| `appName` | object |  |
| `code` | string |  |
| `departmentId` | object |  |
| `externalId` | object |  |
| `mappedIntegration` | object |  |
| `name` | string |  |
| `photoURL` | object |  |
| `replyConfig.acceptsAttachments` | boolean |  |
| `replyConfig.contentTypes[]` | string |  |
| `replyConfig.includeQuotedMessage` | boolean |  |
| `replyConfig.updateRecords` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /channels` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

