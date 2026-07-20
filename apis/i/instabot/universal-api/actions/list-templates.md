# Instabot: List Templates

Retrieves templates from Instabot.

```
GET https://connect.mindcloud.co/v1/universal/instabot/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instabot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instabot/latest/actions/list-templates?${params}`, {
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
      "bot": {
        "objectId": 1
      },
      "description": "string",
      "id": "string",
      "imageFile": {
        "contentType": "string",
        "devCompanyS3Id": "string",
        "isPublic": true,
        "name": "Ava Chen",
        "objectId": 1,
        "s3Id": "string",
        "url": "https://example.com",
        "urlExpiresAt": "2026-05-07T12:00:00.000Z"
      },
      "isActive": true,
      "paymentSubscriptionType": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot.objectId` | number |  |
| `description` | string |  |
| `id` | string |  |
| `imageFile.contentType` | string |  |
| `imageFile.devCompanyS3Id` | string |  |
| `imageFile.isPublic` | boolean |  |
| `imageFile.name` | string |  |
| `imageFile.objectId` | number |  |
| `imageFile.s3Id` | string |  |
| `imageFile.url` | string |  |
| `imageFile.urlExpiresAt` | date |  |
| `isActive` | boolean |  |
| `paymentSubscriptionType` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Instabot API, this operation is `GET /instabot/templates` (base URL `https://api.instabot.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

