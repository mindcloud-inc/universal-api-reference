# <img src="https://images.mindcloud.co/apps/icons/free-linkedin-icon-130-thumb_1772232451132.png" alt="LinkedIn logo" width="28" height="28"> LinkedIn: Universal API

Manage organization posts, comments, images, and profile data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkedin/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.linkedin.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/linkedin/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from LinkedIn. |
| [Get Image](actions/get-image.md) | GET | Retrieves an image from LinkedIn. |
| [Get Video](actions/get-video.md) | GET | Retrieves a video from LinkedIn. |
| [Initialize Document Upload](actions/initialize-document-upload.md) | POST | Initializes a document upload in LinkedIn. |
| [Initialize Image Upload](actions/initialize-image-upload.md) | POST | Initializes an image upload in LinkedIn. |
| [Initialize Video Upload](actions/initialize-video-upload.md) | POST | Initializes a video upload in LinkedIn. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in LinkedIn. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from LinkedIn. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in LinkedIn. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves the authenticated user's profile from LinkedIn. |

