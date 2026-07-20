# <img src="https://images.mindcloud.co/apps/icons/images-10_1776697744552.jpeg" alt="Switchur App logo" width="28" height="28"> Switchur App: Universal API

Interact with a Switchur Switchboard item using credential-backed secure URLs to read the current value or turn the switch on, off, or toggle it.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/switchurApp/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://switchur.com/
- **Vendor API docs:** https://support.switchur.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Switchboard Item Value](actions/get-switchboard-item-value.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/get-switchboard-item-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Set Switchboard Item Value](actions/set-switchboard-item-value.md) | PUT |  |

### Switchboard Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Switchboard Item Value](actions/get-switchboard-item-value.md) | GET |  |
| [Toggle Switch](actions/toggle-switch.md) | PUT |  |
| [Turn Switch Off](actions/turn-switch-off.md) | PUT |  |
| [Turn Switch On](actions/turn-switch-on.md) | PUT |  |

