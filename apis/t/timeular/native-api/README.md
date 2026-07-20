# Timeular: Native API Reference

A consolidated summary of Timeular's API configuration and 113 documented operations, with links to official documentation.

- **Official docs:** https://developers.early.app
- **API base URL:** `https://api.early.app`

## Authentication

### Bearer Access Token

Use a bearer access token generated from the Timeular/EARLY developer sign-in endpoint.

### Credentials

- **Access Token:** `accessToken` · required · Bearer token returned by POST /api/v4/developer/sign-in.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://developers.early.app/)

## Endpoints (113 documented)

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
| [V2 Archive an Activity](actions/v2-archive-an-activity.md) | `DELETE /api/v2/activities/:activityId` | [docs](https://developers.early.app/#22bbcab0-0448-443f-ba64-b640120649cb) |
| [V2 Assign an Activity to Device Side](actions/v2-assign-an-activity-to-device-side.md) | `POST /api/v2/activities/:activityId/device-side/:deviceSideId` | [docs](https://developers.early.app/#db2dea7b-91a9-43ea-ac8f-8c6e90747093) |
| [V2 Create an Activity](actions/v2-create-an-activity.md) | `POST /api/v2/activities` | [docs](https://developers.early.app/#c7afd73f-58ea-4d8f-92b8-ac447aec3ff0) |
| [V2 Create Time Entry](actions/v2-create-time-entry.md) | `POST /api/v2/time-entries` | [docs](https://developers.early.app/#6e2246f2-bd4b-41a6-a3c9-ac8ab53cadc5) |
| [V2 Delete Time Entry](actions/v2-delete-time-entry.md) | `DELETE /api/v2/time-entries/:timeEntryId` | [docs](https://developers.early.app/#0719d2e0-e33a-4162-aef7-4b7590201fc5) |
| [V2 Disable a Device](actions/v2-disable-a-device.md) | `POST /api/v2/devices/:deviceId/disabled` | [docs](https://developers.early.app/#49f9620b-026c-432b-9c27-ae7360141ffe) |
| [V2 Edit a Device](actions/v2-edit-a-device.md) | `PATCH /api/v2/devices/:deviceId` | [docs](https://developers.early.app/#fde0a1f4-eedc-418f-b95d-41cd4e3144ee) |
| [V2 Edit an Activity](actions/v2-edit-an-activity.md) | `PATCH /api/v2/activities/:activityId` | [docs](https://developers.early.app/#e89a59c1-1151-4c52-b1e9-3b9f7f5492b7) |
| [V2 Edit Time Entry](actions/v2-edit-time-entry.md) | `PATCH /api/v2/time-entries/:timeEntryId` | [docs](https://developers.early.app/#2ef8ae40-07ed-49a7-be17-114062abcf32) |
| [V2 Edit Tracking](actions/v2-edit-tracking.md) | `PATCH /api/v2/tracking/:trackingId` | [docs](https://developers.early.app/#623e655f-a6e0-43b6-8c2a-6e7fcccaa4dd) |
| [V2 Enable a Device](actions/v2-enable-a-device.md) | `DELETE /api/v2/devices/:deviceId/disabled` | [docs](https://developers.early.app/#b40aee81-2f6f-4443-ad55-e1623ae58e15) |
| [V2 Fetch Tags & Mentions](actions/v2-fetch-tags-mentions.md) | `GET /api/v2/tags-and-mentions` | [docs](https://developers.early.app/#6caceffc-7c12-4e81-a7e4-3dbc7b08fca1) |
| [V2 Find Time Entries in given range](actions/v2-find-time-entries-in-given-range.md) | `GET /api/v2/time-entries/:start/:end` | [docs](https://developers.early.app/#d950b394-7427-4dae-a9f6-472becc07eda) |
| [V2 Find Time Entry](actions/v2-find-time-entry.md) | `GET /api/v2/time-entries/:timeEntryId` | [docs](https://developers.early.app/#b7e3d7a2-20fe-4c3a-b1e7-5711911bf062) |
| [V2 Generate Report](actions/v2-generate-report.md) | `GET /api/v2/report/:start/:end` | [docs](https://developers.early.app/#dea2c10c-3376-4f43-a2a1-8f8c35fd46a1) |
| [V2 List all Activities](actions/v2-list-all-activities.md) | `GET /api/v2/activities` | [docs](https://developers.early.app/#afae3849-2da7-4203-b452-b829b5203436) |
| [V2 List all Archived Activities](actions/v2-list-all-archived-activities.md) | `GET /api/v2/archived-activities` | [docs](https://developers.early.app/#5e2d2313-a57d-4060-abe1-989d4daca365) |
| [V2 List all known Devices](actions/v2-list-all-known-devices.md) | `GET /api/v2/devices` | [docs](https://developers.early.app/#4fa92072-208c-4d1a-b58d-d64dd9110865) |
| [V2 List enabled Integrations](actions/v2-list-enabled-integrations.md) | `GET /api/v2/integrations` | [docs](https://developers.early.app/#ec63a9c3-ea0d-4415-9797-9bf9707e9e39) |
| [V2 Remove known Device](actions/v2-remove-known-device.md) | `DELETE /api/v2/devices/:deviceId` | [docs](https://developers.early.app/#cf4afb22-657f-483b-abc4-51bead8e5f01) |
| [V2 Removes the active status from the given Device](actions/v2-removes-the-active-status-from-the-given-device.md) | `DELETE /api/v2/devices/:deviceId/active` | [docs](https://developers.early.app/#2a7b6d9b-4adf-4bdb-bf6a-6114a8f2038f) |
| [V2 Sets the status of a Device to active](actions/v2-sets-the-status-of-a-device-to-active.md) | `POST /api/v2/devices/:deviceId/active` | [docs](https://developers.early.app/#460bd3cf-8172-4902-aba8-7425263a82c7) |
| [V2 Show current Tracking](actions/v2-show-current-tracking.md) | `GET /api/v2/tracking` | [docs](https://developers.early.app/#e3edf286-f246-43a4-ae35-9738170ea5c4) |
| [V2 Start Tracking](actions/v2-start-tracking.md) | `POST /api/v2/tracking/:activityId/start` | [docs](https://developers.early.app/#c82fdaee-4545-4a0b-86c5-dfbaa5b831f2) |
| [V2 Stop Tracking](actions/v2-stop-tracking.md) | `POST /api/v2/tracking/:trackingId/stop` | [docs](https://developers.early.app/#311094a8-3290-4735-be03-96953dc3d44b) |
| [V2 Unassign an Activity from a Device Side](actions/v2-unassign-an-activity-from-a-device-side.md) | `DELETE /api/v2/activities/:activityId/device-side/:deviceSideId` | [docs](https://developers.early.app/#1a98f995-a61d-4851-a5d9-1c32367e97d2) |
| [V3 Activate Device](actions/v3-activate-device.md) | `POST /api/v3/devices/:deviceId/activate` | [docs](https://developers.early.app/#2d3946a1-d112-443b-8058-0b27f3fde396) |
| [V3 All Data as JSON](actions/v3-all-data-as-json.md) | `GET /api/v3/report/data/:start/:end` | [docs](https://developers.early.app/#e12c5e47-8f39-4984-b757-798dcbbf2365) |
| [V3 Archive an Activity](actions/v3-archive-an-activity.md) | `DELETE /api/v3/activities/:activityId` | [docs](https://developers.early.app/#234c5874-2086-4104-bff7-af9b9efeced8) |
| [V3 Assign an Activity to Device Side](actions/v3-assign-an-activity-to-device-side.md) | `POST /api/v3/activities/:activityId/device-side/:deviceSideId` | [docs](https://developers.early.app/#8307c8c6-d1d0-476b-abcf-cf76c3d319c0) |
| [V3 Create an Activity](actions/v3-create-an-activity.md) | `POST /api/v3/activities` | [docs](https://developers.early.app/#591f7ca0-7ec5-4c0e-b0d0-99b6967ce53e) |
| [V3 Create Mention](actions/v3-create-mention.md) | `POST /api/v3/mentions` | [docs](https://developers.early.app/#b0de30da-39f4-4d21-b5d5-09e79940c820) |
| [V3 Create Tag](actions/v3-create-tag.md) | `POST /api/v3/tags` | [docs](https://developers.early.app/#d62392ca-2eb2-40c9-8d14-834ba581122e) |
| [V3 Create Time Entry](actions/v3-create-time-entry.md) | `POST /api/v3/time-entries` | [docs](https://developers.early.app/#e66a9e5a-1035-4522-a9fc-5df5a5a05ef7) |
| [V3 Deactivate Device](actions/v3-deactivate-device.md) | `POST /api/v3/devices/:deviceId/deactivate` | [docs](https://developers.early.app/#59928e50-d695-4118-8d71-13079f4ae9d9) |
| [V3 Delete a Time Entry](actions/v3-delete-a-time-entry.md) | `DELETE /api/v3/time-entries/:timeEntryId` | [docs](https://developers.early.app/#a987147c-7c11-4fdc-9ca5-7b03e0999199) |
| [V3 Delete Mention](actions/v3-delete-mention.md) | `DELETE /api/v3/mentions/:mentionId` | [docs](https://developers.early.app/#a7e6b2fa-d879-4368-a4f1-eea14808eef8) |
| [V3 Delete Tag](actions/v3-delete-tag.md) | `DELETE /api/v3/tags/:tagId` | [docs](https://developers.early.app/#c930c6f5-e825-413e-b430-434a05e96e6c) |
| [V3 Disable Device](actions/v3-disable-device.md) | `POST /api/v3/devices/:deviceId/disable` | [docs](https://developers.early.app/#985dae45-b3db-4993-a4b1-5847044388bd) |
| [V3 Edit a Time Entry](actions/v3-edit-a-time-entry.md) | `PATCH /api/v3/time-entries/:timeEntryId` | [docs](https://developers.early.app/#18d45e78-35f7-4dc2-a6c4-edb2405014ed) |
| [V3 Edit an Activity](actions/v3-edit-an-activity.md) | `PATCH /api/v3/activities/:activityId` | [docs](https://developers.early.app/#1ac62610-1bb7-411c-846b-c9690fa3ace5) |
| [V3 Edit Device](actions/v3-edit-device.md) | `PATCH /api/v3/devices/:deviceId` | [docs](https://developers.early.app/#78ab7505-587f-469a-974f-781647bc4900) |
| [V3 Edit Tracking](actions/v3-edit-tracking.md) | `PATCH /api/v3/tracking` | [docs](https://developers.early.app/#52af0d09-fdd8-4095-81bd-d3319cda2c22) |
| [V3 Enable Device](actions/v3-enable-device.md) | `POST /api/v3/devices/:deviceId/enable` | [docs](https://developers.early.app/#96f1eb5b-5aa6-43eb-9176-fd8b7bd5b16f) |
| [V3 Fetch Tags & Mentions](actions/v3-fetch-tags-mentions.md) | `GET /api/v3/tags-and-mentions` | [docs](https://developers.early.app/#03a2a812-cb0a-45e6-8fc6-74a0ff439909) |
| [V3 Find Time Entries in given range](actions/v3-find-time-entries-in-given-range.md) | `GET /api/v3/time-entries/:start/:end` | [docs](https://developers.early.app/#d4c6e3c4-c38b-4891-aa19-907460f43f9b) |
| [V3 Find Time Entry by its ID](actions/v3-find-time-entry-by-its-id.md) | `GET /api/v3/time-entries/:timeEntryId` | [docs](https://developers.early.app/#b4c0569e-a8a7-4c11-9b82-d091bf656812) |
| [V3 Forget Device](actions/v3-forget-device.md) | `DELETE /api/v3/devices/:deviceId` | [docs](https://developers.early.app/#08024987-8f56-41d4-8653-97cbf1202809) |
| [V3 Generate Report](actions/v3-generate-report.md) | `GET /api/v3/report/:start/:end` | [docs](https://developers.early.app/#f9bed9f5-6fbe-4062-9881-76b117430eb2) |
| [V3 List all Activities](actions/v3-list-all-activities.md) | `GET /api/v3/activities` | [docs](https://developers.early.app/#9ac8c381-7e91-4802-8f02-e6918493e902) |
| [V3 List all known Devices](actions/v3-list-all-known-devices.md) | `GET /api/v3/devices` | [docs](https://developers.early.app/#68bff2d1-b66b-4a34-bcf9-0dbd6e0b411b) |
| [V3 List available events](actions/v3-list-available-events.md) | `GET /api/v3/webhooks/event` | [docs](https://developers.early.app/#8a39dd40-8282-4d1e-9315-1945c3117321) |
| [V3 List enabled Integrations](actions/v3-list-enabled-integrations.md) | `GET /api/v3/integrations` | [docs](https://developers.early.app/#cb7bdc76-d2cb-42f8-8f34-fd2fd2488959) |
| [V3 List Subscriptions](actions/v3-list-subscriptions.md) | `GET /api/v3/webhooks/subscription` | [docs](https://developers.early.app/#295fadf6-7f50-48b2-8c1b-daa426046e68) |
| [V3 Me](actions/v3-me.md) | `GET /api/v3/me` | [docs](https://developers.early.app/#bbf459e2-ff90-4aeb-b064-7febaa4eba70) |
| [V3 Show current Tracking](actions/v3-show-current-tracking.md) | `GET /api/v3/tracking` | [docs](https://developers.early.app/#13f48c99-bf92-4892-9f5d-ae17f603526a) |
| [V3 Spaces with Members](actions/v3-spaces-with-members.md) | `GET /api/v3/space` | [docs](https://developers.early.app/#a5bba235-9229-48cb-a5f9-ee557a0bacf9) |
| [V3 Start Tracking](actions/v3-start-tracking.md) | `POST /api/v3/tracking/:activityId/start` | [docs](https://developers.early.app/#4d1dcf30-125a-48d3-8895-27e611581f50) |
| [V3 Stop Tracking](actions/v3-stop-tracking.md) | `POST /api/v3/tracking/stop` | [docs](https://developers.early.app/#329c8b25-a27f-41f9-bdd6-8db04627f0ea) |
| [V3 Subscribe](actions/v3-subscribe.md) | `POST /api/v3/webhooks/subscription` | [docs](https://developers.early.app/#f3ed186d-288f-4a7e-9a35-31c849f936c2) |
| [V3 Unassign an Activity from a Device Side](actions/v3-unassign-an-activity-from-a-device-side.md) | `DELETE /api/v3/activities/:activityId/device-side/:deviceSideId` | [docs](https://developers.early.app/#583e3518-e1df-4a9f-8af7-83efbdd6e79b) |
| [V3 Unsubscribe](actions/v3-unsubscribe.md) | `DELETE /api/v3/webhooks/subscription/:subscriptionId` | [docs](https://developers.early.app/#49f4cefd-7e39-437d-b411-469335b6cb15) |
| [V3 Unsubscribe all for User](actions/v3-unsubscribe-all-for-user.md) | `DELETE /api/v3/webhooks/subscription` | [docs](https://developers.early.app/#3e7db6eb-4bbe-400e-b155-ba7ffde690d4) |
| [V3 Update Mention](actions/v3-update-mention.md) | `PATCH /api/v3/mentions/:mentionId` | [docs](https://developers.early.app/#b00ccf63-701c-471f-abd1-31735f6224d3) |
| [V3 Update Tag](actions/v3-update-tag.md) | `PATCH /api/v3/tags/:tagId` | [docs](https://developers.early.app/#34edd1e9-c5fd-47f3-83a6-bc16e6409d11) |
