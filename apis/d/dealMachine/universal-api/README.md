# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-18-at-16_1773863041812.png" alt="DealMachine logo" width="28" height="28"> DealMachine: Universal API

Manage real estate leads, lists, tags, notes, and mail sequences

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dealMachine/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dealmachine.com
- **Vendor API docs:** https://docs.dealmachine.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lead Statuses](actions/list-lead-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-lead-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | POST |  |
| [Add Lead To Lists](actions/add-lead-to-lists.md) | PUT |  |
| [Add Tags To Lead](actions/add-tags-to-lead.md) | PUT |  |
| [Assign Team Member To Lead](actions/assign-team-member-to-lead.md) | PUT |  |
| [Delete Lead](actions/delete-lead.md) | DELETE |  |
| [End Lead Mail Sequence](actions/end-lead-mail-sequence.md) | PUT |  |
| [Get Lead](actions/get-lead.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |
| [Pause Lead Mail Sequence](actions/pause-lead-mail-sequence.md) | PUT |  |
| [Remove Lead From Lists](actions/remove-lead-from-lists.md) | PUT |  |
| [Remove Tags From Lead](actions/remove-tags-from-lead.md) | PUT |  |
| [Start Lead Mail Sequence](actions/start-lead-mail-sequence.md) | PUT |  |
| [Update Lead Custom Field](actions/update-lead-custom-field.md) | PUT |  |
| [Update Lead Status](actions/update-lead-status.md) | PUT |  |

### Lead Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Note](actions/create-lead-note.md) | POST |  |

### Lead Status

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Statuses](actions/list-lead-statuses.md) | GET |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Lists](actions/list-lists.md) | GET |  |

### Mail Sequence

| Action | Method | Description |
| --- | --- | --- |
| [List Mail Sequences](actions/list-mail-sequences.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET |  |

