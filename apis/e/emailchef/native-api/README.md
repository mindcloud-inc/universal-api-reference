# Emailchef: Native API Reference

A consolidated summary of Emailchef's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://emailchef.com/integration/
- **OpenAPI specification:** https://emailchef.com/integration/data/openapi.yaml
- **API base URL:** `https://app.emailchef.com/apps/api/v1`

## Authentication

### Consumer Key + Consumer Secret

Authenticate with the Consumer Key and Consumer Secret generated in Emailchef.

Send these headers with each API request:

```http
consumerKey: <consumerKey>
consumerSecret: <consumerSecret>
```

[Official authentication documentation](https://emailchef.com/knowledge-base/how-to-generate-api-keys-to-connect-emailchef-plugins/)

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `orderby` in the query string. Set the direction separately with `ordertype`. Use `a` for ascending order and `d` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clone Campaign](actions/clone-campaign.md) | `POST newsletters` | [docs](https://emailchef.com/integration/#/Campaigns/cloneCampaign) |
| [Create Campaign](actions/create-campaign.md) | `POST campaigns` | [docs](https://emailchef.com/integration/#/Campaigns/createCampaign) |
| [Create Contact](actions/create-contact.md) | `POST contacts` | [docs](https://emailchef.com/integration/#/Contacts/createContact) |
| [Create List](actions/create-list.md) | `POST lists` | [docs](https://emailchef.com/integration/#/Lists/createList) |
| [Create Segment](actions/create-segment.md) | `POST segments` | [docs](https://emailchef.com/integration/#/Segments/createSegment) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE campaigns/:id` | [docs](https://emailchef.com/integration/#/Campaigns/deleteCampaign) |
| [Delete List](actions/delete-list.md) | `DELETE lists/:list_id` | [docs](https://emailchef.com/integration/#/Lists/deleteList) |
| [Get Campaign](actions/get-campaign.md) | `GET campaigns/:id` | [docs](https://emailchef.com/integration/#/Campaigns/getCampaign) |
| [Get Contact](actions/get-contact.md) | `GET contacts/:contact_id` | [docs](https://emailchef.com/integration/#/Contacts/getContact) |
| [Get List](actions/get-list.md) | `GET lists/:list_id` | [docs](https://emailchef.com/integration/#/Lists/getList) |
| [Get List Stats](actions/get-list-stats.md) | `GET lists/:list_id/stats` | [docs](https://emailchef.com/integration/#/Lists/getListStats) |
| [Get Segment](actions/get-segment.md) | `GET lists/:list_id/segments/:segment_id` | [docs](https://emailchef.com/integration/#/Segments/getSegment) |
| [Import Contacts](actions/import-contacts.md) | `POST lists/:list_id/import` | [docs](https://emailchef.com/integration/#/Import/importContacts) |
| [List Campaigns](actions/list-campaigns.md) | `GET campaigns` | [docs](https://emailchef.com/integration/#/Campaigns/getCampaigns) |
| [List Contacts](actions/list-contacts.md) | `GET contacts` | [docs](https://emailchef.com/integration/#/Contacts/getContacts) |
| [List Lists](actions/list-lists.md) | `GET lists` | [docs](https://emailchef.com/integration/#/Lists/getLists) |
| [List Segments](actions/list-segments.md) | `GET lists/:list_id/segments` | [docs](https://emailchef.com/integration/#/Segments/getSegments) |
| [Schedule Campaign](actions/schedule-campaign.md) | `PUT campaigns/:id/schedule` | [docs](https://emailchef.com/integration/#/Campaigns/scheduleCampaign) |
| [Send Campaign](actions/send-campaign.md) | `PUT campaigns/:id/send` | [docs](https://emailchef.com/integration/#/Campaigns/sendCampaign) |
| [Send Test Campaign](actions/send-test-campaign.md) | `PUT campaigns/:id/sendtest` | [docs](https://emailchef.com/integration/#/Campaigns/sendTestCampaign) |
| [Unsubscribe Contact From List](actions/unsubscribe-contact-from-list.md) | `POST lists/:list_id/unsubscribe` | [docs](https://emailchef.com/integration/#/Lists/unsubscribeContact) |
| [Update Campaign](actions/update-campaign.md) | `PUT campaigns/:id` | [docs](https://emailchef.com/integration/#/Campaigns/updateCampaign) |
| [Update Contact](actions/update-contact.md) | `PUT contacts/:contact_id` | [docs](https://emailchef.com/integration/#/Contacts/updateContact) |
| [Update List](actions/update-list.md) | `PUT lists/:list_id` | [docs](https://emailchef.com/integration/#/Lists/updateList) |
| [Update Segment](actions/update-segment.md) | `PUT segments/:segment_id` | [docs](https://emailchef.com/integration/#/Segments/updateSegment) |
