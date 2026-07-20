# Federal Communications Commission: Native API Reference

A consolidated summary of Federal Communications Commission's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://publicfiles.fcc.gov/developer
- **API base URL:** `https://publicfiles.fcc.gov`

## Authentication

### API Key

api.data.gov API key used by FCC Public Inspection Files API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.data.gov/docs/developer-manual/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /api/manager/folder/create.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Get Broadcast Contour](actions/get-broadcast-contour.md) | `GET /api/contour/{serviceType}/{idType}/{idValue}.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-contour-apis.json) |
| [Get Cable Details by PSID](actions/get-cable-details-by-psid.md) | `GET /api/service/cable/psid/{psid}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Get Cable Relationship by COALS ID](actions/get-cable-relationship-by-coals-id.md) | `GET /api/service/cable/relationship/username/{COALSID}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Get DBS EEO by Facility](actions/get-dbs-eeo-by-facility.md) | `GET /api/service/dbs/eeo/facility/{facilityID}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Get DBS Entity by FRN](actions/get-dbs-entity-by-frn.md) | `GET /api/service/dbs/frn/{frn}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Get Entity Access Token](actions/get-entity-access-token.md) | `POST /api/manager/get/entityAccessToken.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Get Facility by ID](actions/get-facility-by-id.md) | `GET /api/service/{serviceType}/facility/id/{entityID}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Get File Details](actions/get-file-details.md) | `GET /api/manager/file/id/{fileId}.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Get Folder by ID](actions/get-folder-by-id.md) | `GET /api/manager/folder/id/{folderId}.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Get Folder by Path](actions/get-folder-by-path.md) | `GET /api/manager/folder/path.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Get Relationship by FRN](actions/get-relationship-by-frn.md) | `GET /api/service/relationship/frn/{frn}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Get SDARS EEO by Facility](actions/get-sdars-eeo-by-facility.md) | `GET /api/service/sdars/eeo/facility/{facilityID}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Get SDARS Entity by FRN](actions/get-sdars-entity-by-frn.md) | `GET /api/service/sdars/frn/{frn}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Get Service Relationship by FRN](actions/get-service-relationship-by-frn.md) | `GET /api/service/{serviceType}/relationship/frn/{frn}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [List Cable Communities by PSID](actions/list-cable-communities-by-psid.md) | `GET /api/service/cable/communities/psid/{psid}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [List Cable EEO](actions/list-cable-eeo.md) | `GET /api/service/cable/eeo/{groupBy}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [List Facilities by Service Type](actions/list-facilities-by-service-type.md) | `GET /api/service/{serviceType}/facility/getall` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [List Facility Applications](actions/list-facility-applications.md) | `GET /api/service/{serviceType}/applications/facility/{entityID}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [List Facility EEO](actions/list-facility-eeo.md) | `GET /api/service/{serviceType}/eeo/facilityid/{entityID}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [List Facility Ownership](actions/list-facility-ownership.md) | `GET /api/service/{serviceType}/ownership/facilityid/{entityID}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [List File History](actions/list-file-history.md) | `GET /api/manager/file/history.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [List Folder History](actions/list-folder-history.md) | `GET /api/manager/folder/history.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [List More Public Folders](actions/list-more-public-folders.md) | `GET /api/manager/folder/morePublicFolders.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [List Parent Folders](actions/list-parent-folders.md) | `GET /api/manager/folder/parentFolders.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Move File](actions/move-file.md) | `PUT /api/manager/file/move.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Rename File](actions/rename-file.md) | `PUT /api/manager/file/rename.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Rename Folder](actions/rename-folder.md) | `PUT /api/manager/folder/rename.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Restore File](actions/restore-file.md) | `PUT /api/manager/file/restore.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Restore Folder](actions/restore-folder.md) | `PUT /api/manager/folder/restore.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Search Facilities](actions/search-facilities.md) | `GET /api/service/facility/search/{keyword}` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Search Files and Folders](actions/search-files-and-folders.md) | `GET /api/manager/search/key/{searchKey}.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Update Cable Operator Address](actions/update-cable-operator-address.md) | `POST /api/service/cable/operatorAddress/update` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Update Cable Principal Address](actions/update-cable-principal-address.md) | `POST /api/service/cable/principalAddress/update` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Update Cable Service Employee Units](actions/update-cable-service-employee-units.md) | `POST /api/service/cable/empunitid/update` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Update Cable Service Zip Codes](actions/update-cable-service-zip-codes.md) | `POST /api/service/cable/serviceZipcodes/update` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Update DBS Licensee Address](actions/update-dbs-licensee-address.md) | `POST /api/service/dbs/licenseeAddress/update` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Update SDARS Licensee Address](actions/update-sdars-licensee-address.md) | `POST /api/service/sdars/licenseeAddress/update` | [docs](https://publicfiles.fcc.gov/json/opif-cdbs.json) |
| [Upload Entity Logo](actions/upload-entity-logo.md) | `POST /api/manager/entity/logo/upload` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
| [Upload File](actions/upload-file.md) | `POST /api/manager/file/upload.{format}` | [docs](https://publicfiles.fcc.gov/json/opif-file-manager.json) |
