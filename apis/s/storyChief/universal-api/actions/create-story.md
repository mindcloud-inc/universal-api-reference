# StoryChief: Create Story

Creates a new story in StoryChief.

```
POST https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/create-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/create-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/create-story', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorId` | string | no | Author ID for the story. |
| `content` | string | no | Story HTML content. |
| `excerpt` | string | no | Story excerpt. |
| `language` | string | no | Story language code. |
| `slug` | string | no | Story slug. |
| `sourceId` | string | no | Source ID for the story. |
| `title` | string | no | Story title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {
        "data": {
          "bio": {},
          "email": "ava@example.com",
          "facebookLink": {},
          "firstName": "Ava",
          "id": 1,
          "instagramLink": {},
          "lastName": "Chen",
          "linkedinLink": {},
          "profilePicture": {
            "data": {
              "alt": "string",
              "name": "Ava Chen",
              "sizes": {
                "full": "string",
                "large": "string",
                "regular": "string"
              },
              "url": "https://example.com"
            }
          },
          "twitterLink": {}
        }
      },
      "content": "string",
      "customFields": {
        "data": [
          {
            "description": "string",
            "key": "string",
            "name": "Ava Chen",
            "value": {}
          }
        ]
      },
      "dueAt": {},
      "editUrl": "https://example.com",
      "excerpt": {},
      "id": 1,
      "language": {},
      "publishedAt": {},
      "seoDescription": {},
      "seoKeyword": {},
      "seoTitle": {},
      "slug": "string",
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author.data.bio` | object |  |
| `author.data.email` | string |  |
| `author.data.facebookLink` | object |  |
| `author.data.firstName` | string |  |
| `author.data.id` | number |  |
| `author.data.instagramLink` | object |  |
| `author.data.lastName` | string |  |
| `author.data.linkedinLink` | object |  |
| `author.data.profilePicture.data.alt` | string |  |
| `author.data.profilePicture.data.name` | string |  |
| `author.data.profilePicture.data.sizes.full` | string |  |
| `author.data.profilePicture.data.sizes.large` | string |  |
| `author.data.profilePicture.data.sizes.regular` | string |  |
| `author.data.profilePicture.data.url` | string |  |
| `author.data.twitterLink` | object |  |
| `content` | string |  |
| `customFields.data[].description` | string |  |
| `customFields.data[].key` | string |  |
| `customFields.data[].name` | string |  |
| `customFields.data[].value` | object |  |
| `dueAt` | object |  |
| `editUrl` | string |  |
| `excerpt` | object |  |
| `id` | number |  |
| `language` | object |  |
| `publishedAt` | object |  |
| `seoDescription` | object |  |
| `seoKeyword` | object |  |
| `seoTitle` | object |  |
| `slug` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native StoryChief API, this operation is `POST /stories` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-story.md) for the provider-specific parameters and requirements.

