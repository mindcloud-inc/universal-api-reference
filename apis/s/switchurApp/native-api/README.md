# Switchur App: Native API Reference

A consolidated summary of Switchur App's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://support.switchur.com/
- **API base URL:** `https://api.switchur.com/`

## Authentication

### Tokenized Webhook URLs

Connect a Switchur Switchboard item using its secure On, Off, and Toggle webhook URLs plus the shared item token for reads.

### Credentials

- **Webhook On URL:** `webhookOnUrl` · required · Secure Switchur URL that turns the selected Switchboard item on.
- **Webhook Off URL:** `webhookOffUrl` · required · Secure Switchur URL that turns the selected Switchboard item off.
- **Webhook Toggle URL:** `webhookToggleUrl` · required · Secure Switchur URL that toggles the selected Switchboard item.
- **Switchboard Item Token:** `switchboardItemToken` · required · The unique Switchur token used to read the current value of the selected Switchboard item.

[Official authentication documentation](https://support.switchur.com/)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Switchboard Item Value](actions/get-switchboard-item-value.md) | `GET {{credentials.switchboardItemToken}}` | [docs](https://support.switchur.com/) |
| [Set Switchboard Item Value](actions/set-switchboard-item-value.md) | `PUT /:setToValue/{{credentials.switchboardItemToken}}` | [docs](https://support.switchur.com/) |
| [Toggle Switch](actions/toggle-switch.md) | `PUT {{credentials.webhookToggleUrl}}` | [docs](https://support.switchur.com/) |
| [Turn Switch Off](actions/turn-switch-off.md) | `PUT {{credentials.webhookOffUrl}}` | [docs](https://support.switchur.com/) |
| [Turn Switch On](actions/turn-switch-on.md) | `PUT {{credentials.webhookOnUrl}}` | [docs](https://support.switchur.com/) |
