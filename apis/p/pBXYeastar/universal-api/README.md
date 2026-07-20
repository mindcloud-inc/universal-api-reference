# <img src="https://images.mindcloud.co/apps/icons/p-bxyeastar_1776267520091.png" alt="PBX Yeastar logo" width="28" height="28"> PBX Yeastar: Universal API

Query and manage Yeastar P-Series Cloud PBX data through the PBX OpenAPI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pBXYeastar/latest
- **Category:** Support / Contact Center
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.yeastar.com
- **Vendor API docs:** https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/about-this-guide.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query PBX Information](actions/query-pbx-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-pbx-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Company Contact

| Action | Method | Description |
| --- | --- | --- |
| [Query Company Contact List](actions/query-company-contact-list.md) | GET | Retrieves a list of company contacts from PBX Yeastar. |
| [Search Company Contacts](actions/search-company-contacts.md) | GET | Finds company contacts in PBX Yeastar by search criteria. |

### Extension

| Action | Method | Description |
| --- | --- | --- |
| [Query Extension List](actions/query-extension-list.md) | GET | Retrieves a list of extensions from PBX Yeastar. |
| [Search Extensions](actions/search-extensions.md) | GET | Finds extensions in PBX Yeastar by search criteria. |

### Menu Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Menu Options](actions/get-menu-options.md) | GET | Retrieves menu options from PBX Yeastar. |

### Pbx Capacity

| Action | Method | Description |
| --- | --- | --- |
| [Query PBX Capacity](actions/query-pbx-capacity.md) | GET | Retrieves PBX capacity details from PBX Yeastar. |

### Pbx Information

| Action | Method | Description |
| --- | --- | --- |
| [Query PBX Information](actions/query-pbx-information.md) | GET | Retrieves PBX information from PBX Yeastar. |

### Phonebook

| Action | Method | Description |
| --- | --- | --- |
| [Query Phonebook](actions/query-phonebook.md) | GET | Retrieves a phonebook from PBX Yeastar. |
| [Query Phonebook List](actions/query-phonebook-list.md) | GET | Retrieves a list of phonebooks from PBX Yeastar. |
| [Search Phonebooks](actions/search-phonebooks.md) | GET | Finds phonebooks in PBX Yeastar by search criteria. |

### Queue

| Action | Method | Description |
| --- | --- | --- |
| [Query Queue List](actions/query-queue-list.md) | GET | Retrieves a list of queues from PBX Yeastar. |
| [Search Queues](actions/search-queues.md) | GET | Finds queues in PBX Yeastar by search criteria. |

### Trunk

| Action | Method | Description |
| --- | --- | --- |
| [Query Trunk List](actions/query-trunk-list.md) | GET | Retrieves a list of trunks from PBX Yeastar. |
| [Search Trunks](actions/search-trunks.md) | GET | Finds trunks in PBX Yeastar by search criteria. |

