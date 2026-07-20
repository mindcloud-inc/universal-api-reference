# <img src="https://images.mindcloud.co/apps/icons/subpage_1774884247959.png" alt="Subpage logo" width="28" height="28"> Subpage: Universal API

Create and manage business blogs, help centers, roadmaps, and careers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/subpage/latest
- **Category:** Website & App Building / CMS
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://subpage.app
- **Vendor API docs:** https://helpcenter.subpage.app/article/zapier-api-integration

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/subpage/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [List New Articles](actions/list-new-articles.md) | GET |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [List New Leads](actions/list-new-leads.md) | GET |  |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Trigger Notifications](actions/list-trigger-notifications.md) | GET |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET |  |

