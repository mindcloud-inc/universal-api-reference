# <img src="https://images.mindcloud.co/apps/icons/ubiqod-logo-2_1777931089279.png" alt="Ubiqod by Skiply logo" width="28" height="28"> Ubiqod by Skiply: Universal API

Ubiqod by Skiply connects Skiply IoT buttons, Qods, trackers, sites, badge lists, PIN code lists, and dispatch events to third-party automation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ubiqodBySkiply/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ubiqod.com/
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/ubiqodbyskiply/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Badge Lists](actions/list-badge-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-badge-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Badge List

| Action | Method | Description |
| --- | --- | --- |
| [Add Badges To Badge List](actions/add-badges-to-badge-list.md) | PUT |  |
| [Create Badge List](actions/create-badge-list.md) | POST |  |
| [Delete Badge List](actions/delete-badge-list.md) | DELETE |  |
| [Delete Badges From Badge List](actions/delete-badges-from-badge-list.md) | DELETE |  |
| [List Badge Lists](actions/list-badge-lists.md) | GET |  |
| [Update Badge List](actions/update-badge-list.md) | PUT |  |
| [Update Badges In Badge List](actions/update-badges-in-badge-list.md) | PUT |  |

### Dispatch

| Action | Method | Description |
| --- | --- | --- |
| [List Automation Dispatches](actions/list-automation-dispatches.md) | GET |  |

### Interface

| Action | Method | Description |
| --- | --- | --- |
| [List Interfaces](actions/list-interfaces.md) | GET |  |

### Pin Code List

| Action | Method | Description |
| --- | --- | --- |
| [Add Codes To PIN Code List](actions/add-codes-to-pin-code-list.md) | PUT |  |
| [Create PIN Code List](actions/create-pin-code-list.md) | POST |  |
| [Delete Codes From PIN Code List](actions/delete-codes-from-pin-code-list.md) | DELETE |  |
| [Delete PIN Code List](actions/delete-pin-code-list.md) | DELETE |  |
| [Get PIN Code List](actions/get-pin-code-list.md) | GET |  |
| [List PIN Code Lists](actions/list-pin-code-lists.md) | GET |  |
| [Update Codes In PIN Code List](actions/update-codes-in-pin-code-list.md) | PUT |  |
| [Update PIN Code List](actions/update-pin-code-list.md) | PUT |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST |  |
| [Delete Site](actions/delete-site.md) | DELETE |  |
| [Get Site](actions/get-site.md) | GET |  |
| [List Sites](actions/list-sites.md) | GET |  |
| [Update Site](actions/update-site.md) | PUT |  |

### Tracker

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code Tracker](actions/create-qr-code-tracker.md) | POST |  |
| [Delete Tracker](actions/delete-tracker.md) | DELETE |  |
| [Get Tracker](actions/get-tracker.md) | GET |  |
| [List Trackers](actions/list-trackers.md) | GET |  |
| [Update Tracker](actions/update-tracker.md) | PUT |  |

