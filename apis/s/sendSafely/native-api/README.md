# SendSafely: Native API Reference

A consolidated summary of SendSafely's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://rest-api-docs.sendsafely.com/
- **API base URL:** `https://app.sendsafely.com/api/v2.0`

## Authentication

### API Key

Authenticate SendSafely requests with your API key plus API secret for HMAC request signing.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · Paste the SendSafely API secret that pairs with your API key. MindCloud uses it only to generate the ss-request-signature header.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.sendsafely.com/hc/en-us/articles/360027599232-SendSafely-REST-API)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Group Member](actions/add-contact-group-member.md) | `PUT /group/:groupId/user/` | [docs](https://rest-api-docs.sendsafely.com/#bad5d632-6cca-4d47-bfdd-76efac30b02b) |
| [Add Contact Group to Package](actions/add-contact-group-to-package.md) | `PUT /package/:packageId/group/:groupId/` | [docs](https://rest-api-docs.sendsafely.com/#a4d64acb-eef6-49d0-80be-3a1e93cf0183) |
| [Add File](actions/add-file.md) | `PUT /package/:packageId/file/` | [docs](https://rest-api-docs.sendsafely.com/#56b3d893-ed16-4a97-8746-f8027e0ce250) |
| [Add Recipient](actions/add-recipient.md) | `PUT /package/:packageId/recipient/` | [docs](https://rest-api-docs.sendsafely.com/#3cc9d8e4-b6dc-4b5f-9980-9b1663af465b) |
| [Add Recipients](actions/add-recipients.md) | `PUT /package/:packageId/recipients/` | [docs](https://rest-api-docs.sendsafely.com/#2df2ac0d-a4ad-4ebc-b3c4-ae0a5bf5b19c) |
| [Copy File To Workspace](actions/copy-file-to-workspace.md) | `POST /package/:packageId/file/:fileId/copy/` | [docs](https://rest-api-docs.sendsafely.com/#1310d89a-c507-4d29-86db-a278b8269932) |
| [Create Contact Group](actions/create-contact-group.md) | `PUT /group/` | [docs](https://rest-api-docs.sendsafely.com/#abd6083e-41ce-428c-901a-009968f7bf48) |
| [Create Package](actions/create-package.md) | `PUT /package/` | [docs](https://rest-api-docs.sendsafely.com/#254513ca-04e3-4fb1-b171-2abf2ab36eb7) |
| [Create Subdirectory](actions/create-subdirectory.md) | `PUT /package/:packageId/directory/:directoryId/subdirectory/` | [docs](https://rest-api-docs.sendsafely.com/#66752003-d71c-44e8-a3b5-292b7ed1520b) |
| [Delete Contact Group](actions/delete-contact-group.md) | `DELETE /group/:groupId/` | [docs](https://rest-api-docs.sendsafely.com/#494b46f5-f23f-49fe-b841-78cd42c37b5a) |
| [Delete Contact Group from Package](actions/delete-contact-group-from-package.md) | `DELETE /package/:packageId/group/:groupId/` | [docs](https://rest-api-docs.sendsafely.com/#79ed01aa-9b4f-413f-9a83-20b2866a48db) |
| [Delete Directory](actions/delete-directory.md) | `DELETE /package/:packageId/directory/:directoryId/` | [docs](https://rest-api-docs.sendsafely.com/#e73c740e-8629-4e5d-86ed-c44cbb95f865) |
| [Delete Package](actions/delete-package.md) | `DELETE /package/:packageId/` | [docs](https://rest-api-docs.sendsafely.com/#c162765d-8273-445c-8a6c-740d6eed24ee) |
| [Delete Package File](actions/delete-package-file.md) | `DELETE /package/:packageId/file/:fileId/` | [docs](https://rest-api-docs.sendsafely.com/#484c85ed-d143-4d52-adc1-595a41a82af4) |
| [Delete Recipients](actions/delete-recipients.md) | `DELETE /package/:packageId/recipients/` | [docs](https://rest-api-docs.sendsafely.com/#6463bc5b-8f0a-49fd-bfee-dcd74af8fc5e) |
| [Finalize Package](actions/finalize-package.md) | `POST /package/:packageId/finalize/` | [docs](https://rest-api-docs.sendsafely.com/#330e20d2-06b9-402e-b026-eab2d8e3c936) |
| [Get Contact Group](actions/get-contact-group.md) | `GET /group/:groupId/` | [docs](https://rest-api-docs.sendsafely.com/#35d7a1e1-5e49-48af-9683-f654b127f790) |
| [Get Directory](actions/get-directory.md) | `GET /package/:packageId/directory/:directoryId` | [docs](https://rest-api-docs.sendsafely.com/#3fa8a384-a48b-49fb-9757-8c529e5018cc) |
| [Get File Information](actions/get-file-information.md) | `GET /package/:packageId/file/:fileId/` | [docs](https://rest-api-docs.sendsafely.com/#b139b4ca-fa1a-4cdb-abc1-6f0f94164c79) |
| [Get Package Information](actions/get-package-information.md) | `GET /package/:packageId/` | [docs](https://rest-api-docs.sendsafely.com/#ce95845c-7201-4e30-b820-0ca65868e2c7) |
| [Get Recipient](actions/get-recipient.md) | `GET /package/:packageId/recipient/:recipientId/` | [docs](https://rest-api-docs.sendsafely.com/#14fa5f74-a7d0-4b4f-a324-8c8a94427cf8) |
| [Get User Information](actions/get-user-information.md) | `GET /user/` | [docs](https://rest-api-docs.sendsafely.com/#8cf205c3-b481-445d-8096-d9ccf7aede14) |
| [Get Workspace Activity Log](actions/get-workspace-activity-log.md) | `POST /package/:packageId/activityLog/` | [docs](https://rest-api-docs.sendsafely.com/#3c297ba2-3b34-4786-8dbf-5b7f9bd7147f) |
| [List Archived Packages](actions/list-archived-packages.md) | `GET /package/archived/` | [docs](https://rest-api-docs.sendsafely.com/#48ff3928-81ef-4949-9c20-6a1edc3ff228) |
| [List Collaborators](actions/list-collaborators.md) | `GET /package/:packageId/collaborators` | [docs](https://rest-api-docs.sendsafely.com/#095f1fb2-7813-491b-9793-f543f33b892e) |
| [List Package Permissions](actions/list-package-permissions.md) | `GET /package/:packageId/permissions/` | [docs](https://rest-api-docs.sendsafely.com/#a4c91fca-095c-4d24-a502-49d17c76c05a) |
| [List Received Packages](actions/list-received-packages.md) | `GET /package/received/` | [docs](https://rest-api-docs.sendsafely.com/#ee82b67f-e54e-49a4-b0fa-41dcd18e34d1) |
| [List Sent Packages](actions/list-sent-packages.md) | `GET /package/` | [docs](https://rest-api-docs.sendsafely.com/#294a2831-a410-40c0-beb0-926e97ce4c08) |
| [List User Contact Groups](actions/list-user-contact-groups.md) | `GET /user/groups/` | [docs](https://rest-api-docs.sendsafely.com/#737c997f-50ee-470f-b6b9-5bbb65353f7f) |
| [List Workspace Packages](actions/list-workspace-packages.md) | `GET /package/workspaces/` | [docs](https://rest-api-docs.sendsafely.com/#58a0d150-78b0-4ba4-88eb-9e9aaefe8097) |
| [Move Directory](actions/move-directory.md) | `POST /package/:packageId/move/:sourcedirectoryId/:targetdirectoryId/` | [docs](https://rest-api-docs.sendsafely.com/#e3a8573c-379c-4ce1-a958-b34d4c04f96e) |
| [Move Workspace File](actions/move-workspace-file.md) | `POST /package/:packageId/directory/:directoryId/file/:fileId/` | [docs](https://rest-api-docs.sendsafely.com/#57c14918-e860-4243-b84c-b68c0fd1826a) |
| [Remove Contact Group Member](actions/remove-contact-group-member.md) | `DELETE /group/:groupId/:userId/` | [docs](https://rest-api-docs.sendsafely.com/#9e05e521-c2e2-4f7d-9793-fb90b11effe6) |
| [Remove Recipient](actions/remove-recipient.md) | `DELETE /package/:packageId/recipient/:recipientId/` | [docs](https://rest-api-docs.sendsafely.com/#fb4dc742-c0d6-486a-8e14-ab48bc8acc51) |
| [Rename Directory](actions/rename-directory.md) | `POST /package/:packageId/directory/:directoryId` | [docs](https://rest-api-docs.sendsafely.com/#ae3cb3dc-955e-45c6-a947-9aebc3c09135) |
| [Search Package](actions/search-package.md) | `POST /package/search/` | [docs](https://rest-api-docs.sendsafely.com/#422f4b78-0e8b-42cf-a05e-74329cbfe009) |
| [Update File](actions/update-file.md) | `PATCH /package/:packageId/file/:fileId/` | [docs](https://rest-api-docs.sendsafely.com/#0bce3801-bb2b-4a7f-a4b1-21462aefd100) |
| [Update Package](actions/update-package.md) | `POST /package/:packageId/` | [docs](https://rest-api-docs.sendsafely.com/#77b780f8-b979-4545-892f-f16a18d1f5e2) |
| [Update Recipient](actions/update-recipient.md) | `POST /package/:packageId/recipient/:recipientId/` | [docs](https://rest-api-docs.sendsafely.com/#b47189fb-0922-493c-bafc-99f6bdfbcc21) |
| [Verify Credentials](actions/verify-credentials.md) | `GET /config/verify-credentials/` | [docs](https://rest-api-docs.sendsafely.com/#6ef7285a-d8f7-4bef-b92e-d35f261abb81) |
