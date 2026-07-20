# <img src="https://images.mindcloud.co/apps/icons/federal-communications-commission_1776877927141.png" alt="Federal Communications Commission logo" width="28" height="28"> Federal Communications Commission: Universal API

Access FCC Public Inspection Files APIs for broadcast and cable facility data, contours, public file folders, files, search, history, and supported entity-management operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/federalCommunicationsCommission/latest
- **Category:** Content & Files / Storage
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://publicfiles.fcc.gov/
- **Vendor API docs:** https://publicfiles.fcc.gov/developer

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Facilities](actions/search-facilities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/search-facilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Facility Applications](actions/list-facility-applications.md) | GET | Retrieves FCC facility applications by entity ID. |

### Cable

| Action | Method | Description |
| --- | --- | --- |
| [Get Cable Details by PSID](actions/get-cable-details-by-psid.md) | GET | Retrieves FCC cable details by PSID. |
| [Get Cable Relationship by COALS ID](actions/get-cable-relationship-by-coals-id.md) | GET | Retrieves FCC cable relationships by COALS ID. |
| [List Cable Communities by PSID](actions/list-cable-communities-by-psid.md) | GET | Retrieves FCC cable communities by PSID. |
| [List Cable EEO](actions/list-cable-eeo.md) | GET | Retrieves FCC cable EEO records by grouping. |
| [Update Cable Operator Address](actions/update-cable-operator-address.md) | PUT | Updates an FCC cable operator address. |
| [Update Cable Principal Address](actions/update-cable-principal-address.md) | PUT | Updates an FCC cable principal address. |
| [Update Cable Service Employee Units](actions/update-cable-service-employee-units.md) | PUT | Updates FCC cable service employee units. |
| [Update Cable Service Zip Codes](actions/update-cable-service-zip-codes.md) | PUT | Updates FCC cable service ZIP codes. |

### Contours

| Action | Method | Description |
| --- | --- | --- |
| [Get Broadcast Contour](actions/get-broadcast-contour.md) | GET | Retrieves FCC broadcast contour data by service and identifier. |

### Dbs

| Action | Method | Description |
| --- | --- | --- |
| [Get DBS EEO by Facility](actions/get-dbs-eeo-by-facility.md) | GET | Retrieves FCC DBS EEO records by facility ID. |
| [Get DBS Entity by FRN](actions/get-dbs-entity-by-frn.md) | GET | Retrieves FCC DBS entity details by FRN. |
| [Update DBS Licensee Address](actions/update-dbs-licensee-address.md) | PUT | Updates an FCC DBS licensee address. |

### Entity Access

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity Access Token](actions/get-entity-access-token.md) | GET | Retrieves an FCC entity access token. |

### Facilities

| Action | Method | Description |
| --- | --- | --- |
| [Get Facility by ID](actions/get-facility-by-id.md) | GET | Retrieves an FCC facility by entity ID. |
| [List Facilities by Service Type](actions/list-facilities-by-service-type.md) | GET | Retrieves FCC facilities by service type. |
| [List Facility EEO](actions/list-facility-eeo.md) | GET | Retrieves FCC facility EEO records by entity ID. |
| [List Facility Ownership](actions/list-facility-ownership.md) | GET | Retrieves FCC facility ownership records by entity ID. |
| [Search Facilities](actions/search-facilities.md) | GET | Retrieves FCC facilities matching a keyword. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get File Details](actions/get-file-details.md) | GET | Retrieves FCC OPIF file details by file ID. |
| [List File History](actions/list-file-history.md) | GET | Retrieves FCC OPIF file change history. |
| [Move File](actions/move-file.md) | PUT | Moves an FCC OPIF file to a new folder. |
| [Rename File](actions/rename-file.md) | PUT | Updates the name of an FCC OPIF file. |
| [Restore File](actions/restore-file.md) | PUT | Restores an FCC OPIF file. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to FCC OPIF. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new FCC OPIF folder. |
| [Get Folder by ID](actions/get-folder-by-id.md) | GET | Retrieves an FCC OPIF folder and its contents. |
| [Get Folder by Path](actions/get-folder-by-path.md) | GET | Retrieves an FCC OPIF folder by path. |
| [List Folder History](actions/list-folder-history.md) | GET | Retrieves FCC OPIF folder change history. |
| [List More Public Folders](actions/list-more-public-folders.md) | GET | Retrieves FCC OPIF More Public Files folders. |
| [List Parent Folders](actions/list-parent-folders.md) | GET | Retrieves FCC OPIF parent folders. |
| [Rename Folder](actions/rename-folder.md) | PUT | Updates the name of an FCC OPIF folder. |
| [Restore Folder](actions/restore-folder.md) | PUT | Restores an FCC OPIF folder. |

### Logos

| Action | Method | Description |
| --- | --- | --- |
| [Upload Entity Logo](actions/upload-entity-logo.md) | POST | Uploads an FCC entity logo file. |

### Relationships

| Action | Method | Description |
| --- | --- | --- |
| [Get Relationship by FRN](actions/get-relationship-by-frn.md) | GET | Retrieves FCC relationships by FRN. |
| [Get Service Relationship by FRN](actions/get-service-relationship-by-frn.md) | GET | Retrieves FCC service relationships by FRN. |

### Sdars

| Action | Method | Description |
| --- | --- | --- |
| [Get SDARS EEO by Facility](actions/get-sdars-eeo-by-facility.md) | GET | Retrieves FCC SDARS EEO records by facility ID. |
| [Get SDARS Entity by FRN](actions/get-sdars-entity-by-frn.md) | GET | Retrieves FCC SDARS entity details by FRN. |
| [Update SDARS Licensee Address](actions/update-sdars-licensee-address.md) | PUT | Updates an FCC SDARS licensee address. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Files and Folders](actions/search-files-and-folders.md) | GET | Finds FCC OPIF files and folders by search key. |

