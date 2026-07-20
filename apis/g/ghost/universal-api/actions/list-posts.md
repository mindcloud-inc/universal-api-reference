# Ghost: List Posts

Retrieves posts from Ghost.

```
GET https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-posts?${params}`, {
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
| `filter` | string | no | Ghost filter expression for narrowing posts. |
| `order` | string | no | Ghost order expression for sorting posts. |

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
      "emailOnly": true,
      "emailSegment": "ava@example.com",
      "emailSubject": {},
      "excerpt": "string",
      "featured": true,
      "featureImage": "string",
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
      "primaryTag": {
        "accentColor": {},
        "canonicalUrl": {},
        "codeinjectionFoot": {},
        "codeinjectionHead": {},
        "createdAt": "string",
        "description": {},
        "featureImage": {},
        "id": "string",
        "metaDescription": {},
        "metaTitle": {},
        "name": "Ava Chen",
        "ogDescription": {},
        "ogImage": {},
        "ogTitle": {},
        "slug": "string",
        "twitterDescription": {},
        "twitterImage": {},
        "twitterTitle": {},
        "updatedAt": "string",
        "url": "https://example.com",
        "visibility": "string"
      },
      "publishedAt": "string",
      "readingTime": 1,
      "slug": "string",
      "status": "string",
      "tags": [
        {
          "accentColor": {},
          "canonicalUrl": {},
          "codeinjectionFoot": {},
          "codeinjectionHead": {},
          "createdAt": "string",
          "description": {},
          "featureImage": {},
          "id": "string",
          "metaDescription": {},
          "metaTitle": {},
          "name": "Ava Chen",
          "ogDescription": {},
          "ogImage": {},
          "ogTitle": {},
          "slug": "string",
          "twitterDescription": {},
          "twitterImage": {},
          "twitterTitle": {},
          "updatedAt": "string",
          "url": "https://example.com",
          "visibility": "string"
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
| `emailOnly` | boolean |  |
| `emailSegment` | string |  |
| `emailSubject` | object |  |
| `excerpt` | string |  |
| `featured` | boolean |  |
| `featureImage` | string |  |
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
| `primaryTag.accentColor` | object |  |
| `primaryTag.canonicalUrl` | object |  |
| `primaryTag.codeinjectionFoot` | object |  |
| `primaryTag.codeinjectionHead` | object |  |
| `primaryTag.createdAt` | string |  |
| `primaryTag.description` | object |  |
| `primaryTag.featureImage` | object |  |
| `primaryTag.id` | string |  |
| `primaryTag.metaDescription` | object |  |
| `primaryTag.metaTitle` | object |  |
| `primaryTag.name` | string |  |
| `primaryTag.ogDescription` | object |  |
| `primaryTag.ogImage` | object |  |
| `primaryTag.ogTitle` | object |  |
| `primaryTag.slug` | string |  |
| `primaryTag.twitterDescription` | object |  |
| `primaryTag.twitterImage` | object |  |
| `primaryTag.twitterTitle` | object |  |
| `primaryTag.updatedAt` | string |  |
| `primaryTag.url` | string |  |
| `primaryTag.visibility` | string |  |
| `publishedAt` | string |  |
| `readingTime` | number |  |
| `slug` | string |  |
| `status` | string |  |
| `tags[].accentColor` | object |  |
| `tags[].canonicalUrl` | object |  |
| `tags[].codeinjectionFoot` | object |  |
| `tags[].codeinjectionHead` | object |  |
| `tags[].createdAt` | string |  |
| `tags[].description` | object |  |
| `tags[].featureImage` | object |  |
| `tags[].id` | string |  |
| `tags[].metaDescription` | object |  |
| `tags[].metaTitle` | object |  |
| `tags[].name` | string |  |
| `tags[].ogDescription` | object |  |
| `tags[].ogImage` | object |  |
| `tags[].ogTitle` | object |  |
| `tags[].slug` | string |  |
| `tags[].twitterDescription` | object |  |
| `tags[].twitterImage` | object |  |
| `tags[].twitterTitle` | object |  |
| `tags[].updatedAt` | string |  |
| `tags[].url` | string |  |
| `tags[].visibility` | string |  |
| `title` | string |  |
| `twitterDescription` | object |  |
| `twitterImage` | object |  |
| `twitterTitle` | object |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `uuid` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `GET /posts/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

