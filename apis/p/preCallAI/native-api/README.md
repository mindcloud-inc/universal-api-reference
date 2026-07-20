# PreCallAI: Native API Reference

A consolidated summary of PreCallAI's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.precallai.com/api-reference/introduction
- **API base URL:** `https://api.precallai.com/api/v1`

## Authentication

### API Key

Provide your PreCallAI API key. PreCallAI requires the key in the x-api-key request header for every API call.

### Credentials

- **API Key:** `apiKey` · required · Your PreCallAI API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.precallai.com/api-reference/authorization)

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Upload Segment Contacts](actions/bulk-upload-segment-contacts.md) | `POST /segment/contact/bulk-upload` | [docs](https://docs.precallai.com/api-reference/segments/bulkUpload) |
| [Create Assistant](actions/create-assistant.md) | `POST /user/createAssistant` | [docs](https://docs.precallai.com/api-reference/assistants/create) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaign/create` | [docs](https://docs.precallai.com/api-reference/campaigns/create) |
| [Create Dialer](actions/create-dialer.md) | `POST /dialer/create` | [docs](https://docs.precallai.com/api-reference/dialers/create) |
| [Create Playground](actions/create-playground.md) | `POST /playground/call` | [docs](https://docs.precallai.com/api-reference/playground/create) |
| [Create Segment](actions/create-segment.md) | `POST /segment/create` | [docs](https://docs.precallai.com/api-reference/segments/create) |
| [Create Segment Contact](actions/create-segment-contact.md) | `POST /segment/contact/create` | [docs](https://docs.precallai.com/api-reference/segments/createAudience) |
| [Delete Assistant](actions/delete-assistant.md) | `DELETE /user/deleteassistant` | [docs](https://docs.precallai.com/api-reference/assistants/delete) |
| [Delete Dialer](actions/delete-dialer.md) | `DELETE /dialer/delete` | [docs](https://docs.precallai.com/api-reference/dialers/delete) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /segment/delete` | [docs](https://docs.precallai.com/api-reference/segments/delete) |
| [Delete Segment Contact](actions/delete-segment-contact.md) | `DELETE /segment/contact/delete` | [docs](https://docs.precallai.com/api-reference/segments/deleteAudience) |
| [List Assistants](actions/list-assistants.md) | `GET /user/listAssistant` | [docs](https://docs.precallai.com/api-reference/assistants/get) |
| [List Campaign Contacts](actions/list-campaign-contacts.md) | `POST /campaign/audiences` | [docs](https://docs.precallai.com/api-reference/campaigns/audienceList) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaign/list` | [docs](https://docs.precallai.com/api-reference/campaigns/get) |
| [List Dialers](actions/list-dialers.md) | `GET /dialer/list` | [docs](https://docs.precallai.com/api-reference/dialers/get) |
| [List Playgrounds](actions/list-playgrounds.md) | `GET /playground/list` | [docs](https://docs.precallai.com/api-reference/playground/getHistory) |
| [List Segment Contacts](actions/list-segment-contacts.md) | `GET /segment/contact/list` | [docs](https://docs.precallai.com/api-reference/segments/audienceList) |
| [List Segments](actions/list-segments.md) | `GET /segment/list` | [docs](https://docs.precallai.com/api-reference/segments/get) |
| [Update Assistant](actions/update-assistant.md) | `PUT /user/updateAssistant` | [docs](https://docs.precallai.com/api-reference/assistants/update) |
| [Update Dialer](actions/update-dialer.md) | `PUT /dialer/update` | [docs](https://docs.precallai.com/api-reference/dialers/update) |
| [Update Segment](actions/update-segment.md) | `PUT /segment/update` | [docs](https://docs.precallai.com/api-reference/segments/update) |
| [Update Segment Contact](actions/update-segment-contact.md) | `PUT /segment/contact/update` | [docs](https://docs.precallai.com/api-reference/segments/updateAudience) |
