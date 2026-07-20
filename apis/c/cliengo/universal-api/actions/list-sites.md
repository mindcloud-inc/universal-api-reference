# Cliengo: List Sites



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-sites?${params}`, {
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
      "activeEmailEvents": {},
      "activeWebsiteEmails": true,
      "assignPriority": [
        "string"
      ],
      "autoAssign": [
        "string"
      ],
      "availableSmartTriggers": [
        "string"
      ],
      "companyId": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "email": "ava@example.com",
      "enableChat": true,
      "id": "string",
      "isWhatsAppApi": true,
      "isWhatsAppBusiness": true,
      "isWhatsAppChat": true,
      "isWhatsAppLite": true,
      "labs": {},
      "scriptInstalled": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "url": "https://example.com",
      "webScriptWasCopied": true,
      "whatsAppApiStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeEmailEvents` | object |  |
| `activeWebsiteEmails` | boolean |  |
| `assignPriority` | array<string> |  |
| `autoAssign` | array<string> |  |
| `availableSmartTriggers` | array<string> |  |
| `companyId` | string |  |
| `creationDate` | date |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `enableChat` | boolean |  |
| `id` | string |  |
| `isWhatsAppApi` | boolean |  |
| `isWhatsAppBusiness` | boolean |  |
| `isWhatsAppChat` | boolean |  |
| `isWhatsAppLite` | boolean |  |
| `labs` | object |  |
| `scriptInstalled` | boolean |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `url` | string |  |
| `webScriptWasCopied` | boolean |  |
| `whatsAppApiStatus` | string |  |

## Native endpoint

Through the native Cliengo API, this operation is `GET /sites` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

