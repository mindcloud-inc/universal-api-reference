# Ghost: Update Newsletter

Updates an existing newsletter in Ghost.

```
PUT https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-newsletter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-newsletter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69b0579966c805000821a77d"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-newsletter', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69b0579966c805000821a77d"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ghost newsletter ID from the URL path. Example: `69b0579966c805000821a77d`. |
| `newsletters[0].name` | string | no | Updated public name for the newsletter. Example: `mindcloud`. |
| `newsletters[0].description` | string | no | Updated public description for the newsletter. Example: `Temporary stage 3 description`. |
| `newsletters[0].senderName` | string | no | Updated sender name. Example: `MindCloud`. |
| `newsletters[0].senderEmail` | string | no | Updated sender email address. Example: `newsletter@mindcloud.co`. |
| `newsletters[0].senderReplyTo` | string | no | Updated reply-to behavior for newsletter emails. Example: `newsletter`. |
| `newsletters[0].status` | string | no | Updated newsletter status. Example: `active`. |
| `newsletters[0].subscribeOnSignup` | boolean | no | Whether new members should be subscribed on signup. Example: `true`. |
| `newsletters[0].sortOrder` | number | no | Display order for the newsletter. Example: `0`. |
| `newsletters[0].titleFontCategory` | string | no | Updated title font category. Example: `sans_serif`. |
| `newsletters[0].titleAlignment` | string | no | Updated title alignment. Example: `center`. |
| `newsletters[0].showBadge` | boolean | no | Whether to show the newsletter badge. Example: `true`. |
| `newsletters[0].showHeaderName` | boolean | no | Whether to show the site name in the newsletter header. Example: `false`. |

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

Through the native Ghost API, this operation is `PUT /newsletters/:id/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-newsletter.md) for the provider-specific parameters and requirements.

