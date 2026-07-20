# Ghost Universal API Examples

These examples use the MindCloud API key and Ghost connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Posts

Retrieves posts from Ghost.

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

Example response:

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

See the full [List Posts action reference](actions/list-posts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ghost/latest/actions/list-posts).

## Copy Page

Creates a copy of a page in Ghost.

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

Example response:

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

See the full [Copy Page action reference](actions/copy-page.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ghost/latest/actions/copy-page).
