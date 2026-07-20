# <img src="https://images.mindcloud.co/apps/icons/releasenotes-icon-filled-256_1774566643042.png" alt="ReleaseNotes logo" width="28" height="28"> ReleaseNotes: Universal API

Create, publish, and share product release notes and changelogs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/releaseNotes/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://releasenotes.io
- **Vendor API docs:** https://releasenotes.elevio.help/en/categories/19331-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Latest Release](actions/get-latest-release.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/get-latest-release?connectionId=$CONNECTION_ID&projectId=11233" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Add to Notes Feed](actions/add-to-notes-feed.md) | POST | Creates a new notes feed item in ReleaseNotes. |

### Release

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Release](actions/create-or-update-release.md) | POST | Creates or updates a release in ReleaseNotes. |
| [Get Latest Release](actions/get-latest-release.md) | GET | Retrieves the latest release from ReleaseNotes. |
| [Get Release](actions/get-release.md) | GET | Retrieves a release from ReleaseNotes. |
| [List Releases](actions/list-releases.md) | GET | Retrieves releases from ReleaseNotes. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from ReleaseNotes. |
| [Remove Subscriber](actions/remove-subscriber.md) | DELETE | Deletes a subscriber from ReleaseNotes. |
| [Search Subscribers](actions/search-subscribers.md) | GET | Finds subscribers in ReleaseNotes by search criteria. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in ReleaseNotes. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from ReleaseNotes. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from ReleaseNotes. |

