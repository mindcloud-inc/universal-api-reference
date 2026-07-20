# <img src="https://images.mindcloud.co/apps/icons/content-studio_1775657745466.png" alt="ContentStudio logo" width="28" height="28"> ContentStudio: Universal API

Create, schedule, publish, and analyze social content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/contentStudio/latest
- **Category:** Marketing
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://contentstudio.io
- **Vendor API docs:** https://api-prod.contentstudio.io/guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns for a workspace from ContentStudio. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment to Post](actions/add-comment-to-post.md) | POST | Adds a comment or internal note to a ContentStudio post. |
| [List Post Comments](actions/list-post-comments.md) | GET | Retrieves comments for a post from ContentStudio. |

### Content Category

| Action | Method | Description |
| --- | --- | --- |
| [List Content Categories](actions/list-content-categories.md) | GET | Retrieves content categories for a workspace from ContentStudio. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels for a workspace from ContentStudio. |

### Media Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Media Assets](actions/list-media-assets.md) | GET | Retrieves media assets for a workspace from ContentStudio. |
| [Upload Media](actions/upload-media.md) | POST | Creates a media asset in a ContentStudio workspace. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new social media post in ContentStudio. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes a social media post from ContentStudio, optionally deleting it from platforms. |
| [List Posts](actions/list-posts.md) | GET | Retrieves social media posts for a ContentStudio workspace. |

### Post Approval

| Action | Method | Description |
| --- | --- | --- |
| [Approve or Reject Post](actions/approve-or-reject-post.md) | PUT | Approves or rejects a post under review in ContentStudio. |

### Social Account

| Action | Method | Description |
| --- | --- | --- |
| [List Social Accounts](actions/list-social-accounts.md) | GET | Retrieves social accounts for a workspace from ContentStudio. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members for a workspace from ContentStudio. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from ContentStudio. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces for the authenticated user from ContentStudio. |

