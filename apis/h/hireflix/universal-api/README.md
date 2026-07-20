# <img src="https://images.mindcloud.co/apps/icons/images_1773958814679.jpeg" alt="Hireflix logo" width="28" height="28"> Hireflix: Universal API

Invite candidates, review interviews, and manage hiring workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hireflix/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hireflix.com
- **Vendor API docs:** https://api.hireflix.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Positions](actions/list-positions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from Hireflix. |

### Interview

| Action | Method | Description |
| --- | --- | --- |
| [Get Interview](actions/get-interview.md) | GET | Retrieves an interview from Hireflix. |

### Interview Archive

| Action | Method | Description |
| --- | --- | --- |
| [Archive Interview](actions/archive-interview.md) | PUT | Archives or restores an interview in Hireflix. |

### Interview Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Get Interview Candidate](actions/get-interview-candidate.md) | GET | Retrieves candidate details for an interview in Hireflix. |

### Interview Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Interview Comment](actions/add-interview-comment.md) | POST | Creates an interview comment in Hireflix. |
| [List Interview Comments](actions/list-interview-comments.md) | GET | Retrieves comments for an interview in Hireflix. |

### Interview External Id

| Action | Method | Description |
| --- | --- | --- |
| [Set Interview External ID](actions/set-interview-external-id.md) | PUT | Updates an interview external ID in Hireflix. |

### Interview Finalist

| Action | Method | Description |
| --- | --- | --- |
| [Mark Interview Finalist](actions/mark-interview-finalist.md) | PUT | Updates finalist status for an interview in Hireflix. |

### Interview Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Invite Candidate To Interview](actions/invite-candidate-to-interview.md) | POST | Invites a candidate to an interview in Hireflix. |

### Interview Score

| Action | Method | Description |
| --- | --- | --- |
| [Get Interview Scores](actions/get-interview-scores.md) | GET | Retrieves scoring details for an interview in Hireflix. |
| [Score Interview](actions/score-interview.md) | PUT | Updates an interview score in Hireflix. |

### Interview Share Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Interview Share Link](actions/create-interview-share-link.md) | POST | Creates a shareable interview link in Hireflix. |
| [Remove Interview Share Link](actions/remove-interview-share-link.md) | DELETE | Deletes a shareable interview link from Hireflix. |

### Interview Step

| Action | Method | Description |
| --- | --- | --- |
| [List Interview Steps](actions/list-interview-steps.md) | GET | Retrieves steps for an interview in Hireflix. |

### Interview Thumbnail

| Action | Method | Description |
| --- | --- | --- |
| [Get Interview Thumbnails](actions/get-interview-thumbnails.md) | GET | Retrieves thumbnail images for an interview in Hireflix. |

### Interview Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Interview Tracking](actions/get-interview-tracking.md) | GET | Retrieves tracking events for an interview in Hireflix. |

### Interview User Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Interview User Metadata](actions/get-interview-user-metadata.md) | GET | Retrieves user metadata for an interview in Hireflix. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get Permissions](actions/get-permissions.md) | GET | Retrieves account permissions from Hireflix. |

### Position

| Action | Method | Description |
| --- | --- | --- |
| [Get Position](actions/get-position.md) | GET | Retrieves a position from Hireflix. |
| [List Positions](actions/list-positions.md) | GET | Retrieves positions from Hireflix. |

### Position Interview List

| Action | Method | Description |
| --- | --- | --- |
| [List Position Interviews](actions/list-position-interviews.md) | GET | Retrieves interviews for a position in Hireflix. |

### Position Interview Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Position Interview Stats](actions/get-position-interview-stats.md) | GET | Retrieves interview stats for a position in Hireflix. |

### Position Public Submission

| Action | Method | Description |
| --- | --- | --- |
| [Get Position Public Submission Settings](actions/get-position-public-submission-settings.md) | GET | Retrieves public submission settings for a position in Hireflix. |

### Position Question

| Action | Method | Description |
| --- | --- | --- |
| [List Position Questions](actions/list-position-questions.md) | GET | Retrieves interview questions for a position in Hireflix. |

### Position Shareable Link

| Action | Method | Description |
| --- | --- | --- |
| [List Position Shareable Links](actions/list-position-shareable-links.md) | GET | Retrieves shareable links for a position in Hireflix. |

### Position Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Position Tags](actions/list-position-tags.md) | GET | Retrieves available position tags from Hireflix. |
| [List Tags for Position](actions/list-tags-for-position.md) | GET | Retrieves tags assigned to a position in Hireflix. |

### Position User

| Action | Method | Description |
| --- | --- | --- |
| [List Position Users](actions/list-position-users.md) | GET | Retrieves users assigned to a position in Hireflix. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template by type from Hireflix. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates by type from Hireflix. |

### Theme

| Action | Method | Description |
| --- | --- | --- |
| [Get Theme](actions/get-theme.md) | GET | Retrieves a theme from Hireflix. |
| [List Themes](actions/list-themes.md) | GET | Retrieves themes from Hireflix. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves account usage metrics from Hireflix. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Info](actions/get-current-user-info.md) | GET | Retrieves current user info from Hireflix. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Hireflix. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Hireflix. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Hireflix. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Hireflix. |

### Webhook Log

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Logs](actions/list-webhook-logs.md) | GET | Retrieves webhook logs from Hireflix. |

### Webhook Secret

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Secret Key](actions/get-webhook-secret-key.md) | GET | Retrieves the webhook secret key from Hireflix. |

