# Ghost: Schedule Post

Schedules a post in Ghost.

```
PUT https://connect.mindcloud.co/v1/universal/ghost/latest/actions/schedule-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/schedule-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69b2eb108186310001a3957b",
  "posts[].updatedAt": "2026-03-12T16:34:24.000Z",
  "posts[].publishedAt": "2026-03-13T16:45:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/schedule-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69b2eb108186310001a3957b",
    "posts[].updatedAt": "2026-03-12T16:34:24.000Z",
    "posts[].publishedAt": "2026-03-13T16:45:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ghost post ID to schedule. Example: `69b2eb108186310001a3957b`. |
| `posts[].updatedAt` | string | yes | Current updated timestamp for optimistic locking. Example: `2026-03-12T16:34:24.000Z`. |
| `posts[].publishedAt` | string | yes | Future publish timestamp for the scheduled post. Example: `2026-03-13T16:45:00.000Z`. |

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
        "clicks": 1,
        "negativeFeedback": 1,
        "positiveFeedback": 1
      },
      "createdAt": "string",
      "customExcerpt": {},
      "customTemplate": {},
      "email": {},
      "emailOnly": true,
      "emailSegment": "ava@example.com",
      "emailSubject": {},
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
      "newsletter": {},
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
      "publishedAt": "string",
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
| `count.clicks` | number |  |
| `count.negativeFeedback` | number |  |
| `count.positiveFeedback` | number |  |
| `createdAt` | string |  |
| `customExcerpt` | object |  |
| `customTemplate` | object |  |
| `email` | object |  |
| `emailOnly` | boolean |  |
| `emailSegment` | string |  |
| `emailSubject` | object |  |
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
| `newsletter` | object |  |
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
| `publishedAt` | string |  |
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

Through the native Ghost API, this operation is `PUT /posts/:id/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-post.md) for the provider-specific parameters and requirements.

