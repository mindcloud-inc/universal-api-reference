# MOBIDI: Native API Reference

A consolidated summary of MOBIDI's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://destek.dece.com.tr/space/PAR/1308360709/Mobidi+Office+API+Documentation
- **API base URL:** `https://servis2.dece.com.tr`

## Authentication

### MOBIDI Token

Authenticate MOBIDI requests with a long-lived user token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://decesw.atlassian.net/wiki/spaces/PAR/pages/1277100095/Geodi+Token+Olu%C5%9Fturma)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded; charset=UTF-8` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Sync Health](actions/check-sync-health.md) | `GET /MobidiServerSyncHandler?loginWithGuest=1` | [docs](https://servis2.dece.com.tr/mobidiserversynchandler?op=.wsdl&loginWithGuest=1) |
| [Create Or Update Record](actions/create-or-update-record.md) | `POST /MobidiQueryManagerHandler` | [docs](https://destek.dece.com.tr/space/PAR/1308524567/Mobidi+Server+Create+Update+MobidiEntry+API) |
| [Create Token](actions/create-token.md) | `GET /MobidiTokenHandler` | [docs](https://servis2.dece.com.tr/mobiditokenhandler?op=.wsdl&loginWithGuest=1) |
| [Create Token For User](actions/create-token-for-user.md) | `GET /MobidiTokenHandler` | [docs](https://servis2.dece.com.tr/mobiditokenhandler?op=.wsdl&loginWithGuest=1) |
| [Generate Image Thumbnail](actions/generate-image-thumbnail.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Get Attachment](actions/get-attachment.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Get Mobidi Folder Path](actions/get-mobidi-folder-path.md) | `GET /MobidiSettingsManagerHandler` | [docs](https://servis2.dece.com.tr/mobidisettingsmanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Get New Record Template](actions/get-new-record-template.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Get Next Or Previous Record](actions/get-next-or-previous-record.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Get Record Change Log](actions/get-record-change-log.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Get Record Detail](actions/get-record-detail.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [List All Layers](actions/list-all-layers.md) | `POST /MobidiWorkspaceManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiworkspacemanagerhandler?op=.wsdl&loginWithGuest=1) |
| [List Allowed Login Providers](actions/list-allowed-login-providers.md) | `GET /UserManagementService` | [docs](https://servis2.dece.com.tr/usermanagementservice?op=.wsdl&loginWithGuest=1) |
| [List Dashboards](actions/list-dashboards.md) | `GET /MobidiDashboardHandler` | [docs](https://servis2.dece.com.tr/mobididashboardhandler?op=.wsdl&loginWithGuest=1) |
| [List Saved Queries](actions/list-saved-queries.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Query Record Counts](actions/query-record-counts.md) | `POST /MobidiQueryManagerHandler` | [docs](https://destek.dece.com.tr/space/PAR/1308295209/Mobidi+Server+Query+for+Record+Counts+API) |
| [Query Records](actions/query-records.md) | `POST /MobidiQueryManagerHandler` | [docs](https://destek.dece.com.tr/space/PAR/1308590081/Mobidi+Server+Query+API) |
| [Rotate Image](actions/rotate-image.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Save Layer](actions/save-layer.md) | `POST /MobidiWorkspaceManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiworkspacemanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Save Query For User](actions/save-query-for-user.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Set Default Query](actions/set-default-query.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Update Annotations](actions/update-annotations.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Update Or Delete Saved Query](actions/update-or-delete-saved-query.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /MobidiQueryManagerHandler` | [docs](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1) |
