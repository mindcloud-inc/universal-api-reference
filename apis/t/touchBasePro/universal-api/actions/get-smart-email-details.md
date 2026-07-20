# TouchBasePro: Get Smart Email Details

Retrieves smart email details from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-smart-email-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-smart-email-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-smart-email-details?${params}`, {
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
      "addRecipientsToList": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "properties": {
        "content": {
          "emailVariables": [
            [
              "ava@example.com"
            ]
          ],
          "html": "string",
          "inlineCss": true,
          "text": "string"
        },
        "from": "string",
        "htmlPreviewUrl": "https://example.com",
        "replyTo": "string",
        "subject": "string",
        "textPreviewUrl": "https://example.com"
      },
      "smartEmailId": "ava@example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addRecipientsToList` | string |  |
| `createdAt` | date |  |
| `name` | string |  |
| `properties.content.emailVariables[]` | array<string> |  |
| `properties.content.html` | string |  |
| `properties.content.inlineCss` | boolean |  |
| `properties.content.text` | string |  |
| `properties.from` | string |  |
| `properties.htmlPreviewUrl` | string |  |
| `properties.replyTo` | string |  |
| `properties.subject` | string |  |
| `properties.textPreviewUrl` | string |  |
| `smartEmailId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/transactional/smartEmail/{smartEmailID}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smart-email-details.md) for the provider-specific parameters and requirements.

