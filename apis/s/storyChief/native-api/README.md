# StoryChief: Native API Reference

A consolidated summary of StoryChief's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://developers.storychief.io/
- **API base URL:** `https://api.storychief.io/1.0`

## Authentication

### Bearer Token

Authenticate StoryChief REST API requests with a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.storychief.io/api/collections/3269417/SVmwvHwN?environment=3269417-81fe7caa-52c9-4f28-a4a5-a8a9fd480a8f&segregateAuth=true&versionTag=latest)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.pagination.total_pages`. The current page number is read from `meta.pagination.current_page`.

## Pagination

Use `count` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Author](actions/create-author.md) | `POST /authors` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-2c7072d9-b879-4088-b96d-7fd94ccbdb98) |
| [Create Category](actions/create-category.md) | `POST /categories` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-0b239be8-2419-428a-944a-c9dbb10c3013) |
| [Create Post](actions/create-post.md) | `POST /posts` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-c05bc757-65bc-40d7-80ca-062f5b4dd6f4) |
| [Create Story](actions/create-story.md) | `POST /stories` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-6cb1bcf5-5132-46b5-99b3-ae72705fbd2e) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-17ed9b0a-a92e-4379-961c-65fc30c24f8a) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-970e8e1a-45ab-4a8b-b9f4-ec5d1f409717) |
| [Delete Author](actions/delete-author.md) | `DELETE /authors/:authorId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-b6585c71-de4c-427f-beac-2f8ea8f4e383) |
| [Delete Category](actions/delete-category.md) | `DELETE /categories/:categoryId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-7c43935c-e515-490b-a087-c6c6b023eed5) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:tagId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-d958b83b-bfbc-4350-9d63-7663a373e320) |
| [Get Author](actions/get-author.md) | `GET /authors/:authorId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-5fc1a2a7-c718-4c2e-85f0-bf028cb694ed) |
| [Get Category](actions/get-category.md) | `GET /categories/:categoryId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-8a7a5ef6-0df3-4510-8e79-34980a04b48f) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-52046e84-21fb-4516-9c51-2013f72020b8) |
| [Get Contact List](actions/get-contact-list.md) | `GET /lists/:contactListId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-1958d0cf-b5b4-48b0-bb0f-494f48a1e4e5) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://developers.storychief.io/api/collections/3269417/SVmwvHwN?environment=3269417-81fe7caa-52c9-4f28-a4a5-a8a9fd480a8f&segregateAuth=true&versionTag=latest) |
| [Get Destination](actions/get-destination.md) | `GET /destinations/:destinationId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-8f080722-238f-4ac0-bc5f-809660e09f01) |
| [Get Post](actions/get-post.md) | `GET /posts/:postId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-4b7c9bbd-7979-485f-944a-aad9af869838) |
| [Get Story](actions/get-story.md) | `GET /stories/:storyId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-7fe70109-f48c-499a-9b66-b198d456096e) |
| [Get Story Destination Webhook Payload](actions/get-story-destination-webhook-payload.md) | `GET /stories/:storyId/destinations/:destinationId/webhook` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-06b3e680-ea41-49d2-86bd-de63e6f49351) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tagId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-1ae64576-35c1-42f9-be32-f0f3b59c3093) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-b694f5e4-7154-4396-a120-d481201bb769) |
| [List Authors](actions/list-authors.md) | `GET /authors` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-558eaa32-715c-4e1c-a2b1-bfadf909f7cc) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-ceb18e33-66c3-4efc-979a-9e7a1b967c9c) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /lists` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-ea1e11e1-bd45-42a5-94c0-7b8f858e8762) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-bd3f5551-d685-45a7-9615-640beb300217) |
| [List Destinations](actions/list-destinations.md) | `GET /destinations` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-cb37ebb5-7c32-4b11-8e0e-606589a25319) |
| [List Posts](actions/list-posts.md) | `GET /posts` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-8d5c14c1-658c-4b29-9b6d-a1dee18f4662) |
| [List Stories](actions/list-stories.md) | `GET /stories` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-f369ebc9-08eb-4b19-880a-1028b9052e73) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-a4b6b123-02eb-4d3c-b9dc-de4d0fe6c366) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-df5d5eb4-bc3c-4228-bb67-540c4eb328e4) |
| [Search Contact](actions/search-contact.md) | `POST /contacts/search` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-7134ff82-adf2-48f3-9441-f6463d55434b) |
| [Update Author](actions/update-author.md) | `PUT /authors/:authorId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-834f48fd-2bc1-4559-9dee-fe0780d3e9be) |
| [Update Category](actions/update-category.md) | `PUT /categories/:categoryId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-c5ffbb34-b1b3-4224-addc-68031bf33945) |
| [Update Story](actions/update-story.md) | `PUT /stories/:storyId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-ce0be312-48b9-4f2c-b248-f86d98a765ec) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:tagId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-735a456b-9631-450d-b6e6-6a3d2492bb23) |
| [Update User](actions/update-user.md) | `PUT /users/:userId` | [docs](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-270ccfe0-abf6-4d09-b09a-18c6dc78433e) |
