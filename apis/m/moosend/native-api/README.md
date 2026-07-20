# Moosend: Native API Reference

A consolidated summary of Moosend's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.moosend.com/api-documentation
- **API base URL:** `https://api.moosend.com/v3`

## Authentication

### API Key

Connect with your Moosend API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54552-Authenticate-a-Moosend-API-request?lang=en_US)

## API conventions

Responses from this API use JSON. The total page count is read from `context.paging.totalPageCount`. The current page number is read from `context.paging.currentPage`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Multiple Subscribers](actions/add-multiple-subscribers.md) | `POST /subscribers/{{MailingListID}}/subscribe-many.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54576-Add-multiple-subscribers?lang=en_US) |
| [Add New Subscriber](actions/add-new-subscriber.md) | `POST /subscribers/{{MailingListID}}/subscribe.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54573-Add-a-new-subscriber?lang=en_US) |
| [Add Segment Criteria](actions/add-segment-criteria.md) | `POST /lists/{{MailingListID}}/segments/{{SegmentID}}/criteria/add.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54613-Add-criteria-to-a-segment?lang=en_US) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /lists/{{MailingListID}}/customfields/create.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54564-Create-a-custom-field?lang=en_US) |
| [Create Draft Campaign](actions/create-draft-campaign.md) | `POST /campaigns/create.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54599-Create-a-draft-campaign?lang=en_US) |
| [Create Mailing List](actions/create-mailing-list.md) | `POST /lists/create.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54570-Create-a-mailing-list?lang=en_US) |
| [Create Segment](actions/create-segment.md) | `POST /lists/{{MailingListID}}/segments/create.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54612-Create-an-empty-segment?lang=en_US) |
| [Delete Mailing List](actions/delete-mailing-list.md) | `DELETE /lists/{{MailingListID}}/delete.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54569-Delete-a-mailing-list?lang=en_US) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /lists/{{MailingListID}}/segments/{{SegmentID}}/delete.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54616-Delete-a-segment?lang=en_US) |
| [Get Campaign Details](actions/get-campaign-details.md) | `GET /campaigns/{{CampaignID}}/view.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54586-Get-campaign-details?lang=en_US) |
| [Get Campaign Link Activity](actions/get-campaign-link-activity.md) | `GET /campaigns/{{CampaignID}}/stats/links.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54606-Get-campaign-link-activity?lang=en_US) |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | `GET /campaigns/{{CampaignID}}/stats/{{Type}}.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54605-Get-campaign-statistics?lang=en_US) |
| [Get Campaign Summary](actions/get-campaign-summary.md) | `GET /campaigns/{{CampaignID}}/view-summary.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54604-Get-campaign-summary?lang=en_US) |
| [Get Mailing List Details](actions/get-mailing-list-details.md) | `GET /lists/{{MailingListID}}/details.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54571-Get-mailing-list-details?lang=en_US) |
| [Get Segment Details](actions/get-segment-details.md) | `GET /lists/{{MailingListID}}/segments/{{SegmentID}}/details.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54619-Get-segment-details?lang=en_US) |
| [Get Subscriber By Email Address](actions/get-subscriber-by-email-address.md) | `GET /subscribers/{{MailingListID}}/view.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54581-Get-subscriber-by-email-address?lang=en_US) |
| [Get Subscriber By Id](actions/get-subscriber-by-id.md) | `GET /subscribers/{{MailingListID}}/find/{{SubscriberID}}.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54580-Get-subscriber-by-ID?lang=en_US) |
| [Get Subscriber By Id Without Mailing List Id](actions/get-subscriber-by-id-without-mailing-list-id.md) | `GET /subscribers/{{SubscriberID}}.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54574-Get-subscriber-by-ID-without-mailing-list-ID?lang=en_US) |
| [List Active Mailing Lists](actions/list-active-mailing-lists.md) | `GET /lists.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54568-Get-all-active-mailing-lists?lang=en_US) |
| [List Active Mailing Lists With Paging](actions/list-active-mailing-lists-with-paging.md) | `GET /lists/{{Page}}/{{PageSize}}.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54562-Get-all-active-mailing-lists-with-paging?lang=en_US) |
| [List Campaigns By Page And Page Size](actions/list-campaigns-by-page-and-page-size.md) | `GET /campaigns/{{Page}}/{{PageSize}}.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54585-Get-all-campaigns-by-page-and-page-size?lang=en_US) |
| [List Segment Subscribers](actions/list-segment-subscribers.md) | `GET /lists/{{MailingListID}}/segments/{{SegmentID}}/members.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54618-Get-segment-subscribers?lang=en_US) |
| [List Segments](actions/list-segments.md) | `GET /lists/{{MailingListID}}/segments.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54611-Get-all-segments?lang=en_US) |
| [List Senders](actions/list-senders.md) | `GET /senders/find_all.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54594-Get-all-senders?lang=en_US) |
| [List Subscribers](actions/list-subscribers.md) | `GET /lists/{{MailingListID}}/subscribers/{{Status}}.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54575-Get-all-subscribers?lang=en_US) |
| [Remove Custom Field](actions/remove-custom-field.md) | `DELETE /lists/{{MailingListID}}/customfields/{{CustomFieldID}}/delete.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54566-Remove-a-custom-field?lang=en_US) |
| [Remove Multiple Subscribers](actions/remove-multiple-subscribers.md) | `POST /subscribers/{{MailingListID}}/remove-many.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54591-Remove-multiple-subscribers?lang=en_US) |
| [Remove Subscriber](actions/remove-subscriber.md) | `POST /subscribers/{{MailingListID}}/remove.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54588-Remove-a-subscriber?lang=en_US) |
| [Schedule Campaign](actions/schedule-campaign.md) | `POST /campaigns/{{CampaignID}}/schedule.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54609-Schedule-a-campaign?lang=en_US) |
| [Send Campaign](actions/send-campaign.md) | `POST /campaigns/{{CampaignID}}/send.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54595-Send-a-campaign?lang=en_US) |
| [Test Campaign](actions/test-campaign.md) | `POST /campaigns/{{CampaignID}}/send-test.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54601-Test-a-campaign?lang=en_US) |
| [Unschedule Campaign](actions/unschedule-campaign.md) | `POST /campaigns/{{CampaignID}}/unschedule.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54608-Unschedule-a-campaign?lang=en_US) |
| [Unsubscribe Subscriber From Account](actions/unsubscribe-subscriber-from-account.md) | `POST /subscribers/unsubscribe.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54579-Unsubscribe-a-subscriber-from-an-account?lang=en_US) |
| [Unsubscribe Subscriber From Mailing List](actions/unsubscribe-subscriber-from-mailing-list.md) | `POST /subscribers/{{MailingListID}}/unsubscribe.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54577-Unsubscribe-a-subscriber-from-a-mailing-list?lang=en_US) |
| [Update Custom Field](actions/update-custom-field.md) | `POST /lists/{{MailingListID}}/customfields/{{CustomFieldID}}/update.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54563-Update-a-custom-field?lang=en_US) |
| [Update Draft Campaign](actions/update-draft-campaign.md) | `POST /campaigns/{{CampaignID}}/update.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54598-Update-a-draft-campaign?lang=en_US) |
| [Update Mailing List](actions/update-mailing-list.md) | `POST /lists/{{MailingListID}}/update.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54565-Update-a-mailing-list?lang=en_US) |
| [Update Segment](actions/update-segment.md) | `POST /lists/{{MailingListID}}/segments/{{SegmentID}}/update.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54617-Update-a-segment?lang=en_US) |
| [Update Segment Criteria](actions/update-segment-criteria.md) | `POST /lists/{{MailingListID}}/segments/{{SegmentID}}/criteria/{{CriteriaID}}/update.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54615-Update-segment-criteria?lang=en_US) |
| [Update Subscriber](actions/update-subscriber.md) | `POST /subscribers/{{MailingListID}}/update/{{SubscriberID}}.json` | [docs](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54578-Update-a-subscriber?lang=en_US) |
