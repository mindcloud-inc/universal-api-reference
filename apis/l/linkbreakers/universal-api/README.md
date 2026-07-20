# <img src="https://images.mindcloud.co/apps/icons/linkbreakers-symbol_1776873663088.png" alt="Linkbreakers logo" width="28" height="28"> Linkbreakers: Universal API

Create, track, and manage QR-code links and visitor journeys

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkbreakers/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://linkbreakers.com
- **Vendor API docs:** https://linkbreakers.com/help/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Links](actions/list-links.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Directory

| Action | Method | Description |
| --- | --- | --- |
| [Create a Directory](actions/create-directory.md) | POST | Creates a new directory in Linkbreakers. |
| [List Directories](actions/list-directories.md) | GET | Retrieves a list of directories from Linkbreakers. |
| [Update a Directory](actions/update-directory.md) | PUT | Updates an existing directory in Linkbreakers. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from Linkbreakers. |

### Event Trace

| Action | Method | Description |
| --- | --- | --- |
| [List Event Traces](actions/list-event-traces.md) | GET | Retrieves a list of event traces from Linkbreakers. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Multiple Links](actions/create-multiple-links.md) | POST | Creates multiple new links in Linkbreakers. |
| [Create a New Contact Card Link](actions/create-new-contact-card-link.md) | POST | Creates a new contact card link in Linkbreakers. |
| [Create a New Link](actions/create-new-link.md) | POST | Creates a new link in Linkbreakers. |
| [Delete a Link](actions/delete-link.md) | DELETE | Deletes an existing link from Linkbreakers. |
| [Get Link Details](actions/get-link-details.md) | GET | Retrieves detailed link information from Linkbreakers. |
| [List Links](actions/list-links.md) | GET | Retrieves a list of links from Linkbreakers. |
| [Update a Link](actions/update-link.md) | PUT | Updates an existing link in Linkbreakers. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [List Media Files](actions/list-media-files.md) | GET | Retrieves a list of media files from Linkbreakers. |
| [Upload a Media File](actions/upload-media-file.md) | POST | Uploads a media file to Linkbreakers. |

### Shortlink Availability

| Action | Method | Description |
| --- | --- | --- |
| [Check Shortlink Availability](actions/check-shortlink-availability.md) | GET | Checks whether a shortlink is available in Linkbreakers. |

### Visitor

| Action | Method | Description |
| --- | --- | --- |
| [Get a Visitor](actions/get-visitor.md) | GET | Retrieves detailed visitor information from Linkbreakers. |
| [Identify Visitor](actions/identify-visitor.md) | POST | Identifies a visitor record within Linkbreakers. |
| [List Visitors](actions/list-visitors.md) | GET | Retrieves a list of visitors from Linkbreakers. |
| [Update a Visitor](actions/update-visitor.md) | PUT | Updates an existing visitor in Linkbreakers. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create a Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Linkbreakers. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Linkbreakers. |
| [Update a Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Linkbreakers. |

### Workflow Step

| Action | Method | Description |
| --- | --- | --- |
| [Create a New Workflow Step](actions/create-new-workflow-step.md) | POST | Creates a new workflow step in Linkbreakers. |
| [List Workflow Steps for a Link](actions/list-workflow-steps-for-a-link.md) | GET | Retrieves workflow steps for a link in Linkbreakers. |

