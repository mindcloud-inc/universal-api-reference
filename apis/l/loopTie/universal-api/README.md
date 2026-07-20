# <img src="https://images.mindcloud.co/apps/icons/icon-logo-dark-green_1774903694979.png" alt="Loop & Tie logo" width="28" height="28"> Loop & Tie: Universal API

Loop & Tie is a corporate gifting platform API for managing teams, collections, designs, gifts, surveys, templates, packaging bundles, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loopTie/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.loopandtie.com
- **Vendor API docs:** https://docs.loopandtie.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Design](actions/create-design.md) | POST | Creates a new design in Loop & Tie. |
| [List Designs](actions/list-designs.md) | GET | Retrieves designs for a Loop & Tie team. |
| [List Logos](actions/list-logos.md) | GET | Retrieves logos for a Loop & Tie team. |
| [Upload Logo](actions/upload-logo.md) | POST | Creates a new logo in Loop & Tie. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [List Packaging Bundles](actions/list-packaging-bundles.md) | GET | Retrieves packaging bundles for a Loop & Tie team. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET | Retrieves product collections for a Loop & Tie team. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves gift messages for a Loop & Tie team. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Schedulers](actions/list-schedulers.md) | GET | Retrieves schedulers for a Loop & Tie team. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams available in Loop & Tie. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates for a Loop & Tie team. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Gifts](actions/bulk-create-gifts.md) | POST | Creates multiple gifts at once in Loop & Tie. |
| [Cancel Gift](actions/cancel-gift.md) | DELETE | Cancels an unredeemed gift in Loop & Tie. |
| [Create Gift](actions/create-gift.md) | POST | Creates a new gift in Loop & Tie. |
| [Get Gift](actions/get-gift.md) | GET | Retrieves a gift from Loop & Tie. |
| [List Gifts](actions/list-gifts.md) | GET | Retrieves gifts sent by a Loop & Tie team. |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys for a Loop & Tie team. |
| [Preview Gifts](actions/preview-gifts.md) | POST | Creates gift preview links in Loop & Tie. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Loop & Tie. |
| [Delete Webhook By URL](actions/delete-webhook-by-url.md) | DELETE | Deletes a webhook from Loop & Tie by URL. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook URLs for a Loop & Tie team. |

