# <img src="https://images.mindcloud.co/apps/icons/story-chief_1778083178178.png" alt="StoryChief logo" width="28" height="28"> StoryChief: Universal API

Plan, create, publish, and analyze content campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/storyChief/latest
- **Category:** Marketing
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.storychief.io/
- **Vendor API docs:** https://developers.storychief.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Author

| Action | Method | Description |
| --- | --- | --- |
| [Create Author](actions/create-author.md) | POST | Creates a new author in StoryChief. |
| [Delete Author](actions/delete-author.md) | DELETE | Deletes an author from StoryChief. |
| [Get Author](actions/get-author.md) | GET | Retrieves an author from StoryChief. |
| [List Authors](actions/list-authors.md) | GET | Retrieves authors from StoryChief. |
| [Update Author](actions/update-author.md) | PUT | Updates an existing author in StoryChief. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in StoryChief. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes a category from StoryChief. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from StoryChief. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from StoryChief. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in StoryChief. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from StoryChief. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from StoryChief. |
| [Search Contact](actions/search-contact.md) | GET | Finds contacts in StoryChief. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from StoryChief. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from StoryChief. |

### Destination

| Action | Method | Description |
| --- | --- | --- |
| [Get Destination](actions/get-destination.md) | GET | Retrieves a destination from StoryChief. |
| [List Destinations](actions/list-destinations.md) | GET | Retrieves destinations from StoryChief. |

### Destination Webhook Payload

| Action | Method | Description |
| --- | --- | --- |
| [Get Story Destination Webhook Payload](actions/get-story-destination-webhook-payload.md) | GET | Retrieves a story destination webhook payload from StoryChief. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in StoryChief. |
| [Get Post](actions/get-post.md) | GET | Retrieves a post from StoryChief. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from StoryChief. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Create Story](actions/create-story.md) | POST | Creates a new story in StoryChief. |
| [Get Story](actions/get-story.md) | GET | Retrieves a story from StoryChief. |
| [List Stories](actions/list-stories.md) | GET | Retrieves stories from StoryChief. |
| [Update Story](actions/update-story.md) | PUT | Updates an existing story in StoryChief. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in StoryChief. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes a tag from StoryChief. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from StoryChief. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from StoryChief. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in StoryChief. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in StoryChief. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from StoryChief. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from StoryChief. |
| [List Users](actions/list-users.md) | GET | Retrieves users from StoryChief. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in StoryChief. |

