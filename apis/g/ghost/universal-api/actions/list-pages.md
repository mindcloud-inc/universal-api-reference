# Ghost: List Pages

Retrieves pages from Ghost.

```
GET https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-pages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated related resources to include. |
| `formats` | string | no | Comma-separated content formats to return. |
| `filter` | string | no | Ghost filter expression for narrowing pages. |
| `order` | string | no | Ghost order expression for sorting pages. |

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
      "createdAt": "string",
      "customExcerpt": {},
      "customTemplate": {},
      "excerpt": "string",
      "featured": true,
      "featureImage": {},
      "featureImageAlt": {},
      "featureImageCaption": {},
      "frontmatter": {},
      "id": "string",
      "lexical": {},
      "metaDescription": {},
      "metaTitle": {},
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
      "readingTime": 1,
      "showTitleAndFeatureImage": true,
      "slug": "string",
      "status": "string",
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
| `createdAt` | string |  |
| `customExcerpt` | object |  |
| `customTemplate` | object |  |
| `excerpt` | string |  |
| `featured` | boolean |  |
| `featureImage` | object |  |
| `featureImageAlt` | object |  |
| `featureImageCaption` | object |  |
| `frontmatter` | object |  |
| `id` | string |  |
| `lexical` | object |  |
| `metaDescription` | object |  |
| `metaTitle` | object |  |
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
| `readingTime` | number |  |
| `showTitleAndFeatureImage` | boolean |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `twitterDescription` | object |  |
| `twitterImage` | object |  |
| `twitterTitle` | object |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `uuid` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `GET /pages/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

