# Ghost: List Newsletters

Retrieves newsletters from Ghost.

```
GET https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-newsletters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-newsletters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-newsletters?${params}`, {
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
      "backgroundColor": "string",
      "bodyFontCategory": "string",
      "buttonColor": "string",
      "buttonCorners": "string",
      "buttonStyle": "string",
      "createdAt": "string",
      "description": {},
      "dividerColor": {},
      "feedbackEnabled": true,
      "footerContent": {},
      "headerBackgroundColor": "string",
      "headerImage": {},
      "id": "string",
      "imageCorners": "string",
      "linkColor": "https://example.com",
      "linkStyle": "https://example.com",
      "name": "Ava Chen",
      "postTitleColor": {},
      "sectionTitleColor": {},
      "senderEmail": {},
      "senderName": {},
      "senderReplyTo": "string",
      "showBadge": true,
      "showCommentCta": true,
      "showExcerpt": true,
      "showFeatureImage": true,
      "showHeaderIcon": true,
      "showHeaderName": true,
      "showHeaderTitle": true,
      "showLatestPosts": true,
      "showPostTitleSection": true,
      "showSubscriptionDetails": true,
      "slug": "string",
      "sortOrder": 1,
      "status": "string",
      "subscribeOnSignup": true,
      "titleAlignment": "string",
      "titleFontCategory": "string",
      "titleFontWeight": "string",
      "updatedAt": "string",
      "uuid": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundColor` | string |  |
| `bodyFontCategory` | string |  |
| `buttonColor` | string |  |
| `buttonCorners` | string |  |
| `buttonStyle` | string |  |
| `createdAt` | string |  |
| `description` | object |  |
| `dividerColor` | object |  |
| `feedbackEnabled` | boolean |  |
| `footerContent` | object |  |
| `headerBackgroundColor` | string |  |
| `headerImage` | object |  |
| `id` | string |  |
| `imageCorners` | string |  |
| `linkColor` | string |  |
| `linkStyle` | string |  |
| `name` | string |  |
| `postTitleColor` | object |  |
| `sectionTitleColor` | object |  |
| `senderEmail` | object |  |
| `senderName` | object |  |
| `senderReplyTo` | string |  |
| `showBadge` | boolean |  |
| `showCommentCta` | boolean |  |
| `showExcerpt` | boolean |  |
| `showFeatureImage` | boolean |  |
| `showHeaderIcon` | boolean |  |
| `showHeaderName` | boolean |  |
| `showHeaderTitle` | boolean |  |
| `showLatestPosts` | boolean |  |
| `showPostTitleSection` | boolean |  |
| `showSubscriptionDetails` | boolean |  |
| `slug` | string |  |
| `sortOrder` | number |  |
| `status` | string |  |
| `subscribeOnSignup` | boolean |  |
| `titleAlignment` | string |  |
| `titleFontCategory` | string |  |
| `titleFontWeight` | string |  |
| `updatedAt` | string |  |
| `uuid` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `GET /newsletters/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-newsletters.md) for the provider-specific parameters and requirements.

