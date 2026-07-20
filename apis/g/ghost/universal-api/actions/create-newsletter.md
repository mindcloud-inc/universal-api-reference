# Ghost: Create Newsletter

Creates a new newsletter in Ghost.

```
POST https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-newsletter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-newsletter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "newsletters[0].name": "Ghost Stage 3 Test Newsletter"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-newsletter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "newsletters[0].name": "Ghost Stage 3 Test Newsletter"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `newsletters[0].name` | string | yes | Public name for the newsletter. Example: `Ghost Stage 3 Test Newsletter`. |
| `newsletters[0].description` | string | no | Public description for the newsletter. Example: `Temporary stage 3 newsletter`. |
| `newsletters[0].senderReplyTo` | string | no | Reply-to behavior for newsletter emails. Example: `newsletter`. |
| `newsletters[0].status` | string | no | Newsletter status. Example: `active`. |
| `newsletters[0].subscribeOnSignup` | boolean | no | Whether new members should be subscribed on signup. Example: `false`. |
| `newsletters[0].showHeaderName` | boolean | no | Whether to show the site name in the newsletter header. Example: `false`. |
| `newsletters[0].titleFontCategory` | string | no | Title font category, such as sans_serif. Example: `sans_serif`. |
| `newsletters[0].titleAlignment` | string | no | Title alignment, such as center. Example: `center`. |
| `newsletters[0].showBadge` | boolean | no | Whether to show the newsletter badge. Example: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optInExisting` | boolean | no | Whether existing members should be opted into the new newsletter. Example: `false`. |

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

Through the native Ghost API, this operation is `POST /newsletters/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-newsletter.md) for the provider-specific parameters and requirements.

