# <img src="https://images.mindcloud.co/apps/icons/atlas-airevenue-engine_1773946182468.png" alt="Atlas AI Revenue Engine logo" width="28" height="28"> Atlas AI Revenue Engine: Universal API

Manage Atlas campaigns, calls, bookings, and knowledge files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/atlasAIRevenueEngine/latest
- **Category:** Support / Contact Center
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://youratlas.com
- **Vendor API docs:** https://apidocs.youratlas.com/what-can-you-build-with-the-atlas-api-2063751m0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Call Bookings](actions/list-call-bookings.md) | GET |  |
| [List Campaign Bookings](actions/list-campaign-bookings.md) | GET |  |

### Call Record

| Action | Method | Description |
| --- | --- | --- |
| [Delete Call Record](actions/delete-call-record.md) | DELETE |  |
| [Get Call Record](actions/get-call-record.md) | GET |  |
| [List Call Records](actions/list-call-records.md) | GET |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Delete Campaign](actions/delete-campaign.md) | DELETE |  |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [List Knowledge Base File Linked Campaigns](actions/list-knowledge-base-file-linked-campaigns.md) | GET |  |
| [Set Campaign Status](actions/set-campaign-status.md) | PUT |  |
| [Update Campaign](actions/update-campaign.md) | PUT |  |

### Knowledge Base File

| Action | Method | Description |
| --- | --- | --- |
| [Add Knowledge Base File to Collection](actions/add-knowledge-base-file-to-collection.md) | POST |  |
| [Attach Knowledge Base File to Campaign](actions/attach-knowledge-base-file-to-campaign.md) | POST |  |
| [Delete Knowledge Base File](actions/delete-knowledge-base-file.md) | DELETE |  |
| [Detach Knowledge Base File from Campaign](actions/detach-knowledge-base-file-from-campaign.md) | DELETE |  |
| [List Campaign Knowledge Base Files](actions/list-campaign-knowledge-base-files.md) | GET |  |
| [List Knowledge Base Files](actions/list-knowledge-base-files.md) | GET |  |
| [Remove Knowledge Base File from Collection](actions/remove-knowledge-base-file-from-collection.md) | DELETE |  |
| [Upload Knowledge Base File](actions/upload-knowledge-base-file.md) | POST |  |
| [Upload Knowledge from URL](actions/upload-knowledge-from-url.md) | POST |  |

### Scheduled Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Scheduled Call](actions/create-scheduled-call.md) | POST |  |
| [List Scheduled Calls](actions/list-scheduled-calls.md) | GET |  |

### Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | GET |  |
| [List Campaign Overview Statistics](actions/list-campaign-overview-statistics.md) | GET |  |

