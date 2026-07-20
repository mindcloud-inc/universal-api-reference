# <img src="https://images.mindcloud.co/apps/icons/images-1_1773522974147.png" alt="CleverReach logo" width="28" height="28"> CleverReach: Universal API

Create newsletters, automate campaigns, and manage recipients in CleverReach

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cleverReach/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cleverreach.com/
- **Vendor API docs:** https://rest.cleverreach.com/explorer/v3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups](actions/list-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Get Attribute Limits](actions/get-attribute-limits.md) | GET | Retrieves account attribute limits from CleverReach. |
| [List Attributes](actions/list-attributes.md) | GET | Retrieves local and global attributes from CleverReach. |

### Blacklist Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Blacklist Entry](actions/get-blacklist-entry.md) | GET | Retrieves a blacklist entry from CleverReach by email address. |
| [List Blacklist Entries](actions/list-blacklist-entries.md) | GET | Retrieves blacklisted email entries from CleverReach. |

### Bounce

| Action | Method | Description |
| --- | --- | --- |
| [List Bounces](actions/list-bounces.md) | GET | Retrieves account bounce records from CleverReach. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a deprecated form from CleverReach. |
| [Get Form Embedded Code](actions/get-form-embedded-code.md) | GET | Retrieves deprecated embedded form code from CleverReach. |
| [List Forms](actions/list-forms.md) | GET | Retrieves deprecated signup forms from CleverReach. |
| [List Group Forms](actions/list-group-forms.md) | GET | Retrieves deprecated group forms from CleverReach. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from CleverReach by group ID. |
| [Get Group Stats](actions/get-group-stats.md) | GET | Retrieves statistics for a group in CleverReach. |
| [List Groups](actions/list-groups.md) | GET | Retrieves receiver groups from your CleverReach account. |

### Group Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Group Attributes](actions/list-group-attributes.md) | GET | Retrieves local group attributes from CleverReach. |

### Group Filter

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Filter](actions/get-group-filter.md) | GET | Retrieves a group filter from CleverReach. |
| [Get Group Filter Stats](actions/get-group-filter-stats.md) | GET | Retrieves statistics for a group filter in CleverReach. |
| [List Group Filters](actions/list-group-filters.md) | GET | Retrieves saved group filters from CleverReach. |

### Mailing

| Action | Method | Description |
| --- | --- | --- |
| [Get Mailing](actions/get-mailing.md) | GET | Retrieves a mailing from CleverReach by mailing ID. |
| [List Mailing Links](actions/list-mailing-links.md) | GET | Retrieves links for a mailing in CleverReach. |
| [List Mailings](actions/list-mailings.md) | GET | Retrieves mailings from your CleverReach account. |

### Receiver

| Action | Method | Description |
| --- | --- | --- |
| [Count Group Filter Receivers](actions/count-group-filter-receivers.md) | GET | Retrieves a receiver count for a group filter in CleverReach. |
| [Get Group Receiver](actions/get-group-receiver.md) | GET | Retrieves a group receiver from CleverReach. |
| [Get Receiver](actions/get-receiver.md) | GET | Retrieves a receiver from CleverReach by receiver ID. |
| [List Group Filter Receivers](actions/list-group-filter-receivers.md) | GET | Retrieves group filter receivers from CleverReach. |
| [List Group Receivers](actions/list-group-receivers.md) | GET | Retrieves receivers for a group in CleverReach. |
| [List Receiver Groups](actions/list-receiver-groups.md) | GET | Retrieves groups for a receiver in CleverReach. |

### Receiver Event

| Action | Method | Description |
| --- | --- | --- |
| [List Group Receiver Events](actions/list-group-receiver-events.md) | GET | Retrieves receiver events for a group receiver in CleverReach. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Report](actions/get-report.md) | GET | Retrieves a report from CleverReach by report ID. |
| [Get Report Stats](actions/get-report-stats.md) | GET | Retrieves report statistics from CleverReach by reporting mode. |
| [List Report Receivers by State](actions/list-report-receivers-by-state.md) | GET | Retrieves report receivers from CleverReach by delivery state. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from your CleverReach account. |

