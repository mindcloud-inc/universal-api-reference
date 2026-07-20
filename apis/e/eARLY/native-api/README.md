# EARLY: Native API Reference

A consolidated summary of EARLY's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://developers.early.app/
- **API base URL:** `https://api.early.app`

## Authentication

### Bearer Token

Use an EARLY bearer access token. Generate it outside MindCloud by calling POST /api/v4/developer/sign-in with your API key and API secret, then paste the returned token here.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.early.app/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Member to Folder](actions/add-member-to-folder.md) | `POST /api/v4/folders/:folderId/members` | [docs](https://developers.early.app/#379ec93f-802b-43f7-a12c-c7bbf7b51555) |
| [Approve Leave](actions/approve-leave.md) | `POST /api/v4/leaves/:leaveId/approve` | [docs](https://developers.early.app/#cdcda8e5-030d-42e7-8dee-84c4954a589a) |
| [Archive Activity](actions/archive-activity.md) | `DELETE /api/v4/activities/:activityId` | [docs](https://developers.early.app/#be926b1a-5aaa-403f-b8b0-576b8772538f) |
| [Archive Folder](actions/archive-folder.md) | `POST /api/v4/folders/:folderId/archive` | [docs](https://developers.early.app/#2c15cd2d-baca-4e36-936b-377c03ad3081) |
| [Cancel Tracking](actions/cancel-tracking.md) | `DELETE /api/v4/tracking` | [docs](https://developers.early.app/#344a5b26-cbf5-49a7-a7f1-0bbfe4b03766) |
| [Create Activity](actions/create-activity.md) | `POST /api/v4/activities` | [docs](https://developers.early.app/#21afd678-09fc-449e-974e-1734196d7124) |
| [Create Folder](actions/create-folder.md) | `POST /api/v4/folders` | [docs](https://developers.early.app/#b80bf1bb-2a8f-4124-91d7-d4a9ed024080) |
| [Create Leave](actions/create-leave.md) | `POST /api/v4/leaves` | [docs](https://developers.early.app/#ea85a312-9df6-4248-a6ab-3fabec54360b) |
| [Create Leave for User](actions/create-leave-for-user.md) | `POST /api/v4/users/:userId/leaves` | [docs](https://developers.early.app/#1f769296-6d23-4a4e-b15a-401dd4e2dd30) |
| [Create Mention](actions/create-mention.md) | `POST /api/v4/mentions` | [docs](https://developers.early.app/#23643fec-12a2-4fa2-8c72-d57f7fe96682) |
| [Create Tag](actions/create-tag.md) | `POST /api/v4/tags` | [docs](https://developers.early.app/#c23b9b70-b888-43dc-ab74-5cddd3c3e581) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /api/v4/time-entries` | [docs](https://developers.early.app/#192b7ce9-d25e-42ff-8c03-b9d06a9b0b75) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /api/v4/webhooks/subscription` | [docs](https://developers.early.app/#1f0ca463-6396-4be9-b62e-fa60d274e1ff) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /api/v4/folders/:folderId` | [docs](https://developers.early.app/#bc2aaae1-35e9-42ee-be7f-8b07d27c9afd) |
| [Delete Leave](actions/delete-leave.md) | `DELETE /api/v4/leaves/:leaveId` | [docs](https://developers.early.app/#f7989f80-9e76-4838-a273-dc31fd0e7288) |
| [Delete Mention](actions/delete-mention.md) | `DELETE /api/v4/mentions/:mentionId` | [docs](https://developers.early.app/#27d62d2f-97f0-49bf-bfa5-e7292ff1d421) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /api/v4/tags/:tagId` | [docs](https://developers.early.app/#ac8eba90-6107-46c4-89e3-7babdaeefc9d) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /api/v4/time-entries/:timeEntryId` | [docs](https://developers.early.app/#ad0986b6-aae6-4b25-acc2-333b6822b6e6) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /api/v4/webhooks/subscription/:subscriptionId` | [docs](https://developers.early.app/#ad4c3dd7-bb28-447f-a6bc-147928d230e4) |
| [Delete Webhook Subscriptions for User](actions/delete-webhook-subscriptions-for-user.md) | `DELETE /api/v4/webhooks/subscription` | [docs](https://developers.early.app/#04443b18-b9e7-468e-8723-192747b28521) |
| [Deny Leave](actions/deny-leave.md) | `POST /api/v4/leaves/:leaveId/deny` | [docs](https://developers.early.app/#e4256be7-7d98-4f32-a0ed-2cb26c551074) |
| [Generate Report](actions/generate-report.md) | `POST /api/v4/report` | [docs](https://developers.early.app/#04fcb4f6-7a83-4117-91dc-1e9ab75b0519) |
| [Get Current Tracking](actions/get-current-tracking.md) | `GET /api/v4/tracking` | [docs](https://developers.early.app/#2ff32590-05f3-42f4-91dc-df6b6e32c135) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v4/me` | [docs](https://developers.early.app/#1e7dfdde-e619-4a82-b9c8-88c5e39c0e95) |
| [Get Folder](actions/get-folder.md) | `GET /api/v4/folders/:folderId` | [docs](https://developers.early.app/#29cb8ee4-ff3b-46d1-aa87-7bb3abe2c0f3) |
| [Get Folder Member](actions/get-folder-member.md) | `GET /api/v4/folders/:folderId/members/:memberId` | [docs](https://developers.early.app/#20a5dd57-d697-4d85-ad19-04b47a500eee) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /api/v4/time-entries/:timeEntryId` | [docs](https://developers.early.app/#73ff0de6-42ba-4386-986c-5f83f7ef1372) |
| [List Activities](actions/list-activities.md) | `GET /api/v4/activities` | [docs](https://developers.early.app/#ef363185-8b39-4fbf-b03b-458291ee324a) |
| [List available Webhook Events](actions/list-available-webhook-events.md) | `GET /api/v4/webhooks/event` | [docs](https://developers.early.app/#cc25a42c-45fb-4ba0-a259-0927f00b8b3d) |
| [List Folder Members](actions/list-folder-members.md) | `GET /api/v4/folders/:folderId/members` | [docs](https://developers.early.app/#2d4b52d1-df46-48c6-9e02-4475fb613793) |
| [List Folders](actions/list-folders.md) | `GET /api/v4/folders` | [docs](https://developers.early.app/#dbd5c8f0-bb89-4eb8-b9c4-0175bc05a8f8) |
| [List Leave Types](actions/list-leave-types.md) | `GET /api/v4/leaves/types` | [docs](https://developers.early.app/#d0bdc2e8-7e8d-47cb-ba40-da3fdf4ff8e5) |
| [List Leaves](actions/list-leaves.md) | `GET /api/v4/leaves` | [docs](https://developers.early.app/#1b9995fe-89e4-41aa-9e74-cbb41e360eb3) |
| [List Tags and Mentions](actions/list-tags-and-mentions.md) | `GET /api/v4/tags-and-mentions` | [docs](https://developers.early.app/#fe2e519d-21bc-45f6-aec7-927635e77d7d) |
| [List Time Entries in Range](actions/list-time-entries-in-range.md) | `GET /api/v4/time-entries/:start/:end` | [docs](https://developers.early.app/#98b4f754-ebcd-4706-b9b0-93244c24e033) |
| [List Users](actions/list-users.md) | `GET /api/v4/users` | [docs](https://developers.early.app/#89798c88-eee0-429a-adae-3c9b4e7d8fe2) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /api/v4/webhooks/subscription` | [docs](https://developers.early.app/#f6353878-4147-462e-b702-a3fc97a0926f) |
| [Remove Member from Folder](actions/remove-member-from-folder.md) | `DELETE /api/v4/folders/:folderId/members/:memberId` | [docs](https://developers.early.app/#a1e03e9c-cf98-460c-ae95-e1b3626304b6) |
| [Start Tracking](actions/start-tracking.md) | `POST /api/v4/tracking/:activityId/start` | [docs](https://developers.early.app/#ffc19f68-496d-4a78-9ec1-bd2f21739aee) |
| [Stop Tracking](actions/stop-tracking.md) | `POST /api/v4/tracking/stop` | [docs](https://developers.early.app/#b5f602d3-cc31-4a03-abd9-9fa397121ab5) |
| [Unarchive Activity](actions/unarchive-activity.md) | `POST /api/v4/activities/:activityId/unarchive` | [docs](https://developers.early.app/#6f5b8cb5-dc7a-4258-a855-3d160203a893) |
| [Unarchive Folder](actions/unarchive-folder.md) | `POST /api/v4/folders/:folderId/unarchive` | [docs](https://developers.early.app/#c71538c6-d899-48ef-a38b-3c5a8c2699f4) |
| [Update Activity](actions/update-activity.md) | `PATCH /api/v4/activities/:activityId` | [docs](https://developers.early.app/#45a1b847-5182-4fe3-ac01-5a0ac0e811d3) |
| [Update Folder](actions/update-folder.md) | `PATCH /api/v4/folders/:folderId` | [docs](https://developers.early.app/#40d2035a-6b0d-4b68-9259-6a4779a8928c) |
| [Update Mention](actions/update-mention.md) | `PATCH /api/v4/mentions/:mentionId` | [docs](https://developers.early.app/#e0d26363-ad2a-493c-a118-7f61e270e7ee) |
| [Update Tag](actions/update-tag.md) | `PATCH /api/v4/tags/:tagId` | [docs](https://developers.early.app/#2baca20f-6988-4f14-8b4b-3fbcbb5a81b9) |
| [Update Time Entry](actions/update-time-entry.md) | `PATCH /api/v4/time-entries/:timeEntryId` | [docs](https://developers.early.app/#8420ac26-ff58-43fa-aa10-5a58042346c2) |
| [Update Tracking](actions/update-tracking.md) | `PATCH /api/v4/tracking` | [docs](https://developers.early.app/#5b5b08ff-3ddc-4fd7-bfb4-1ae0f990c87c) |
