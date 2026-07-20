# Ghost: Copy Page

Creates a copy of a page in Ghost.

```
POST https://connect.mindcloud.co/v1/universal/ghost/latest/actions/copy-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/copy-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/copy-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ghost page ID to copy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        {
          "accessibility": "string",
          "bio": {},
          "bluesky": {},
          "commentNotifications": true,
          "coverImage": {},
          "createdAt": "string",
          "donationNotifications": true,
          "email": "ava@example.com",
          "facebook": {},
          "freeMemberSignupNotification": true,
          "id": "string",
          "instagram": {},
          "lastSeen": "string",
          "linkedin": {},
          "location": {},
          "mastodon": {},
          "mentionNotifications": true,
          "metaDescription": {},
          "metaTitle": {},
          "milestoneNotifications": true,
          "name": "Ava Chen",
          "paidSubscriptionCanceledNotification": true,
          "paidSubscriptionStartedNotification": true,
          "profileImage": {},
          "recommendationNotifications": true,
          "roles": [
            {
              "createdAt": "string",
              "description": "string",
              "id": "string",
              "name": "Ava Chen",
              "updatedAt": "string"
            }
          ],
          "slug": "string",
          "status": "string",
          "threads": {},
          "tiktok": {},
          "tour": {},
          "twitter": {},
          "updatedAt": "string",
          "url": "https://example.com",
          "website": {},
          "youtube": {}
        }
      ],
      "canonicalUrl": {},
      "codeinjectionFoot": {},
      "codeinjectionHead": {},
      "commentId": "string",
      "count": {
        "negativeFeedback": 1,
        "paidConversions": 1,
        "positiveFeedback": 1,
        "signups": 1
      },
      "createdAt": "string",
      "customExcerpt": {},
      "customTemplate": {},
      "excerpt": {},
      "featured": true,
      "featureImage": {},
      "featureImageAlt": {},
      "featureImageCaption": {},
      "frontmatter": {},
      "id": "string",
      "lexical": "string",
      "metaDescription": {},
      "metaTitle": {},
      "mobiledoc": {},
      "ogDescription": {},
      "ogImage": {},
      "ogTitle": {},
      "primaryAuthor": {
        "accessibility": "string",
        "bio": {},
        "bluesky": {},
        "commentNotifications": true,
        "coverImage": {},
        "createdAt": "string",
        "donationNotifications": true,
        "email": "ava@example.com",
        "facebook": {},
        "freeMemberSignupNotification": true,
        "id": "string",
        "instagram": {},
        "lastSeen": "string",
        "linkedin": {},
        "location": {},
        "mastodon": {},
        "mentionNotifications": true,
        "metaDescription": {},
        "metaTitle": {},
        "milestoneNotifications": true,
        "name": "Ava Chen",
        "paidSubscriptionCanceledNotification": true,
        "paidSubscriptionStartedNotification": true,
        "profileImage": {},
        "recommendationNotifications": true,
        "roles": [
          {
            "createdAt": "string",
            "description": "string",
            "id": "string",
            "name": "Ava Chen",
            "updatedAt": "string"
          }
        ],
        "slug": "string",
        "status": "string",
        "threads": {},
        "tiktok": {},
        "tour": {},
        "twitter": {},
        "updatedAt": "string",
        "url": "https://example.com",
        "website": {},
        "youtube": {}
      },
      "primaryTag": {},
      "publishedAt": {},
      "showTitleAndFeatureImage": true,
      "slug": "string",
      "status": "string",
      "tiers": [
        {
          "active": true,
          "createdAt": "string",
          "currency": {},
          "description": {},
          "id": "string",
          "monthlyPrice": {},
          "monthlyPriceId": {},
          "name": "Ava Chen",
          "slug": "string",
          "trialDays": 1,
          "type": "string",
          "updatedAt": "string",
          "visibility": "string",
          "welcomePageUrl": {},
          "yearlyPrice": {},
          "yearlyPriceId": {}
        }
      ],
      "title": "string",
      "twitterDescription": {},
      "twitterImage": {},
      "twitterTitle": {},
      "updatedAt": "string",
      "url": "https://example.com",
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
| `authors[].accessibility` | string |  |
| `authors[].bio` | object |  |
| `authors[].bluesky` | object |  |
| `authors[].commentNotifications` | boolean |  |
| `authors[].coverImage` | object |  |
| `authors[].createdAt` | string |  |
| `authors[].donationNotifications` | boolean |  |
| `authors[].email` | string |  |
| `authors[].facebook` | object |  |
| `authors[].freeMemberSignupNotification` | boolean |  |
| `authors[].id` | string |  |
| `authors[].instagram` | object |  |
| `authors[].lastSeen` | string |  |
| `authors[].linkedin` | object |  |
| `authors[].location` | object |  |
| `authors[].mastodon` | object |  |
| `authors[].mentionNotifications` | boolean |  |
| `authors[].metaDescription` | object |  |
| `authors[].metaTitle` | object |  |
| `authors[].milestoneNotifications` | boolean |  |
| `authors[].name` | string |  |
| `authors[].paidSubscriptionCanceledNotification` | boolean |  |
| `authors[].paidSubscriptionStartedNotification` | boolean |  |
| `authors[].profileImage` | object |  |
| `authors[].recommendationNotifications` | boolean |  |
| `authors[].roles[].createdAt` | string |  |
| `authors[].roles[].description` | string |  |
| `authors[].roles[].id` | string |  |
| `authors[].roles[].name` | string |  |
| `authors[].roles[].updatedAt` | string |  |
| `authors[].slug` | string |  |
| `authors[].status` | string |  |
| `authors[].threads` | object |  |
| `authors[].tiktok` | object |  |
| `authors[].tour` | object |  |
| `authors[].twitter` | object |  |
| `authors[].updatedAt` | string |  |
| `authors[].url` | string |  |
| `authors[].website` | object |  |
| `authors[].youtube` | object |  |
| `canonicalUrl` | object |  |
| `codeinjectionFoot` | object |  |
| `codeinjectionHead` | object |  |
| `commentId` | string |  |
| `count.negativeFeedback` | number |  |
| `count.paidConversions` | number |  |
| `count.positiveFeedback` | number |  |
| `count.signups` | number |  |
| `createdAt` | string |  |
| `customExcerpt` | object |  |
| `customTemplate` | object |  |
| `excerpt` | object |  |
| `featured` | boolean |  |
| `featureImage` | object |  |
| `featureImageAlt` | object |  |
| `featureImageCaption` | object |  |
| `frontmatter` | object |  |
| `id` | string |  |
| `lexical` | string |  |
| `metaDescription` | object |  |
| `metaTitle` | object |  |
| `mobiledoc` | object |  |
| `ogDescription` | object |  |
| `ogImage` | object |  |
| `ogTitle` | object |  |
| `primaryAuthor.accessibility` | string |  |
| `primaryAuthor.bio` | object |  |
| `primaryAuthor.bluesky` | object |  |
| `primaryAuthor.commentNotifications` | boolean |  |
| `primaryAuthor.coverImage` | object |  |
| `primaryAuthor.createdAt` | string |  |
| `primaryAuthor.donationNotifications` | boolean |  |
| `primaryAuthor.email` | string |  |
| `primaryAuthor.facebook` | object |  |
| `primaryAuthor.freeMemberSignupNotification` | boolean |  |
| `primaryAuthor.id` | string |  |
| `primaryAuthor.instagram` | object |  |
| `primaryAuthor.lastSeen` | string |  |
| `primaryAuthor.linkedin` | object |  |
| `primaryAuthor.location` | object |  |
| `primaryAuthor.mastodon` | object |  |
| `primaryAuthor.mentionNotifications` | boolean |  |
| `primaryAuthor.metaDescription` | object |  |
| `primaryAuthor.metaTitle` | object |  |
| `primaryAuthor.milestoneNotifications` | boolean |  |
| `primaryAuthor.name` | string |  |
| `primaryAuthor.paidSubscriptionCanceledNotification` | boolean |  |
| `primaryAuthor.paidSubscriptionStartedNotification` | boolean |  |
| `primaryAuthor.profileImage` | object |  |
| `primaryAuthor.recommendationNotifications` | boolean |  |
| `primaryAuthor.roles[].createdAt` | string |  |
| `primaryAuthor.roles[].description` | string |  |
| `primaryAuthor.roles[].id` | string |  |
| `primaryAuthor.roles[].name` | string |  |
| `primaryAuthor.roles[].updatedAt` | string |  |
| `primaryAuthor.slug` | string |  |
| `primaryAuthor.status` | string |  |
| `primaryAuthor.threads` | object |  |
| `primaryAuthor.tiktok` | object |  |
| `primaryAuthor.tour` | object |  |
| `primaryAuthor.twitter` | object |  |
| `primaryAuthor.updatedAt` | string |  |
| `primaryAuthor.url` | string |  |
| `primaryAuthor.website` | object |  |
| `primaryAuthor.youtube` | object |  |
| `primaryTag` | object |  |
| `publishedAt` | object |  |
| `showTitleAndFeatureImage` | boolean |  |
| `slug` | string |  |
| `status` | string |  |
| `tiers[].active` | boolean |  |
| `tiers[].createdAt` | string |  |
| `tiers[].currency` | object |  |
| `tiers[].description` | object |  |
| `tiers[].id` | string |  |
| `tiers[].monthlyPrice` | object |  |
| `tiers[].monthlyPriceId` | object |  |
| `tiers[].name` | string |  |
| `tiers[].slug` | string |  |
| `tiers[].trialDays` | number |  |
| `tiers[].type` | string |  |
| `tiers[].updatedAt` | string |  |
| `tiers[].visibility` | string |  |
| `tiers[].welcomePageUrl` | object |  |
| `tiers[].yearlyPrice` | object |  |
| `tiers[].yearlyPriceId` | object |  |
| `title` | string |  |
| `twitterDescription` | object |  |
| `twitterImage` | object |  |
| `twitterTitle` | object |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `uuid` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `POST /pages/:id/copy` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-page.md) for the provider-specific parameters and requirements.

