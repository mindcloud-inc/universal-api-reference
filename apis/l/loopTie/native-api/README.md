# Loop & Tie: Native API Reference

A consolidated summary of Loop & Tie's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.loopandtie.com/reference
- **API base URL:** `https://api.loopandtie.com/v1`

## Authentication

### Access Token

Authenticate with one Loop & Tie access token sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.loopandtie.com/reference/oauth-20-api-access)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Create Gifts](actions/bulk-create-gifts.md) | `POST /teams/:teamId/bulk/gifts` | [docs](https://docs.loopandtie.com/reference/teamsteam_idgifts-2) |
| [Cancel Gift](actions/cancel-gift.md) | `DELETE /teams/:teamId/gifts/:giftId` | [docs](https://docs.loopandtie.com/reference/teamsteam_idgiftsid-1) |
| [Create Design](actions/create-design.md) | `POST /teams/:teamId/designs` | [docs](https://docs.loopandtie.com/reference/teamsteam_iddesigns-1) |
| [Create Gift](actions/create-gift.md) | `POST /teams/:teamId/gifts` | [docs](https://docs.loopandtie.com/reference/teamsteam_idgifts-1) |
| [Create Webhook](actions/create-webhook.md) | `POST /teams/:teamId/hooks` | [docs](https://docs.loopandtie.com/reference/teamsteam_idhooks) |
| [Delete Webhook By URL](actions/delete-webhook-by-url.md) | `DELETE /teams/:teamId/hooks` | [docs](https://docs.loopandtie.com/reference/teamsteam_idhooks-2) |
| [Get Gift](actions/get-gift.md) | `GET /teams/:teamId/gifts/:giftId` | [docs](https://docs.loopandtie.com/reference/teamsteam_idgiftsid) |
| [List Collections](actions/list-collections.md) | `GET /teams/:teamId/collections` | [docs](https://docs.loopandtie.com/reference/teamsteam_idcollections) |
| [List Designs](actions/list-designs.md) | `GET /teams/:teamId/designs` | [docs](https://docs.loopandtie.com/reference/teamsteam_iddesigns) |
| [List Gifts](actions/list-gifts.md) | `GET /teams/:teamId/gifts` | [docs](https://docs.loopandtie.com/reference/teamsteam_idgifts) |
| [List Logos](actions/list-logos.md) | `GET /teams/:teamId/logos` | [docs](https://docs.loopandtie.com/reference/teamsteam_idlogos) |
| [List Messages](actions/list-messages.md) | `GET /teams/:teamId/messages` | [docs](https://docs.loopandtie.com/reference/teamsteam_idmessages) |
| [List Packaging Bundles](actions/list-packaging-bundles.md) | `GET /teams/:teamId/custom-packaging-bundles` | [docs](https://docs.loopandtie.com/reference/teamsteam_idcustom-packaging-bundles) |
| [List Schedulers](actions/list-schedulers.md) | `GET /teams/:teamId/schedulers` | [docs](https://docs.loopandtie.com/reference/teamsteam_idschedulers) |
| [List Surveys](actions/list-surveys.md) | `GET /teams/:teamId/surveys` | [docs](https://docs.loopandtie.com/reference/teamsteam_idsurveys) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://docs.loopandtie.com/reference/teams) |
| [List Templates](actions/list-templates.md) | `GET /teams/:teamId/templates` | [docs](https://docs.loopandtie.com/reference/teamsteam_idtemplates) |
| [List Webhooks](actions/list-webhooks.md) | `GET /teams/:teamId/hooks` | [docs](https://docs.loopandtie.com/reference/teamsteam_idhooks-1) |
| [Preview Gifts](actions/preview-gifts.md) | `POST /teams/:teamId/previews` | [docs](https://docs.loopandtie.com/reference/teamsteam_idpreviews) |
| [Upload Logo](actions/upload-logo.md) | `POST /teams/:teamId/logos` | [docs](https://docs.loopandtie.com/reference/teamsteam_idlogos-1) |
