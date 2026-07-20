# Yay.com: Native API Reference

A consolidated summary of Yay.com's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://www.yay.com/voip/api-docs/
- **API base URL:** `https://api.yay.com`

## Authentication

### Custom Header Auth

Use Yay reseller credentials in request headers.

### Credentials

- **Reseller:** `reseller` · required · Reseller identifier from the Yay dashboard.
- **User:** `user` · required · Reseller API user from the Yay dashboard.
- **Password:** `password` · required · Reseller API password from the Yay dashboard.

Send these headers with each API request:

```http
X-Auth-User: <user>
X-Auth-Password: <password>
X-Auth-Reseller: <reseller>
```

[Official authentication documentation](https://www.yay.com/blog/api/beginners-guide-part-1/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud 1.0` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | `GET /account/balance` | [docs](https://www.yay.com/voip/api-docs/account/account-reseller-balance/) |
| [Get Call Recording Retention](actions/get-call-recording-retention.md) | `GET /voip/call-retention` | [docs](https://www.yay.com/voip/api-docs/calls/call-retention/) |
| [Get Maximum Call Cost Restriction](actions/get-maximum-call-cost-restriction.md) | `GET /voip/call-restrictions/max-call-cost` | [docs](https://www.yay.com/voip/api-docs/calls/call-restriction/) |
| [Get Next Call Flow Extension](actions/get-next-call-flow-extension.md) | `GET /voip/next-extension/flow` | [docs](https://www.yay.com/voip/api-docs/numbers/call-route/) |
| [Get Next Hunt Group Extension](actions/get-next-hunt-group-extension.md) | `GET /voip/next-extension/group` | [docs](https://www.yay.com/voip/api-docs/users/hunt-group/) |
| [Get Next Mailbox Menu Extension](actions/get-next-mailbox-menu-extension.md) | `GET /voip/next-extension/mailbox-menu` | [docs](https://www.yay.com/voip/api-docs/mailbox/mailbox-menu/) |
| [Get Next SIP User Extension](actions/get-next-sip-user-extension.md) | `GET /voip/next-extension/user` | [docs](https://www.yay.com/voip/api-docs/users/sip-user/) |
| [List Allowed International Call Exceptions](actions/list-allowed-international-call-exceptions.md) | `GET /voip/call-restrictions/international-exception` | [docs](https://www.yay.com/voip/api-docs/calls/call-restriction/) |
| [List Call Flows](actions/list-call-flows.md) | `GET /voip/flow` | [docs](https://www.yay.com/voip/api-docs/numbers/call-route/) |
| [List Call Packs](actions/list-call-packs.md) | `GET /voip/call-pack` | [docs](https://www.yay.com/voip/api-docs/calls/call-packs/) |
| [List Call Restriction Patterns](actions/list-call-restriction-patterns.md) | `GET /voip/call-restrictions/call-pattern` | [docs](https://www.yay.com/voip/api-docs/calls/call-restriction/) |
| [List Call Statistics Schedules](actions/list-call-statistics-schedules.md) | `GET /voip/call/statistics/schedule` | [docs](https://www.yay.com/voip/api-docs/calls/call-statistics-schedule/) |
| [List Caller ID Requests](actions/list-caller-id-requests.md) | `GET /voip/cli-request` | [docs](https://www.yay.com/voip/api-docs/caller-id/cli-request/) |
| [List Caller IDs](actions/list-caller-ids.md) | `GET /voip/caller-id` | [docs](https://www.yay.com/voip/api-docs/caller-id/cli/) |
| [List Departments](actions/list-departments.md) | `GET /voip/department` | [docs](https://www.yay.com/voip/api-docs/users/department/) |
| [List Documents](actions/list-documents.md) | `GET /account/document` | [docs](https://www.yay.com/voip/api-docs/account/document/) |
| [List Emergency Addresses](actions/list-emergency-addresses.md) | `GET /voip/emergency-address` | [docs](https://www.yay.com/voip/api-docs/numbers/emergency-address/) |
| [List Hunt Groups](actions/list-hunt-groups.md) | `GET /voip/group` | [docs](https://www.yay.com/voip/api-docs/users/hunt-group/) |
| [List Integrations](actions/list-integrations.md) | `GET /account/integration` | [docs](https://www.yay.com/voip/api-docs/account/account-integration/) |
| [List Mailbox Menus](actions/list-mailbox-menus.md) | `GET /voip/mailbox-menu` | [docs](https://www.yay.com/voip/api-docs/mailbox/mailbox-menu/) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /voip/mailbox` | [docs](https://www.yay.com/voip/api-docs/mailbox/mailbox/) |
| [List Message Flows](actions/list-message-flows.md) | `GET /voip/message-flow` | [docs](https://www.yay.com/voip/api-docs/numbers/message-route/) |
| [List Missed Call Notifications](actions/list-missed-call-notifications.md) | `GET /voip/missed-call` | [docs](https://www.yay.com/voip/api-docs/calls/call-missed-notification/) |
| [List Number Addresses](actions/list-number-addresses.md) | `GET /voip/number-address` | [docs](https://www.yay.com/voip/api-docs/numbers/number-address/) |
| [List Phone Books](actions/list-phone-books.md) | `GET /voip/phone-book` | [docs](https://www.yay.com/voip/api-docs/phone-books/phone-book/) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /voip/number` | [docs](https://www.yay.com/voip/api-docs/numbers/number/) |
| [List Playlists](actions/list-playlists.md) | `GET /voip/playlist` | [docs](https://www.yay.com/voip/api-docs/audio/playlist/) |
| [List Provisioning Devices](actions/list-provisioning-devices.md) | `GET /provisioning/device` | [docs](https://www.yay.com/voip/api-docs/provisioning/provisioning-device/) |
| [List Reseller Addresses](actions/list-reseller-addresses.md) | `GET /account/reseller-address` | [docs](https://www.yay.com/voip/api-docs/account/account-reseller-address/) |
| [List Reseller Users](actions/list-reseller-users.md) | `GET /account/reseller-user` | [docs](https://www.yay.com/voip/api-docs/account/account-reseller-user/) |
| [List Short Codes](actions/list-short-codes.md) | `GET /voip/short-code` | [docs](https://www.yay.com/voip/api-docs/short-code/short-code/) |
| [List SIP User Statuses](actions/list-sip-user-statuses.md) | `GET /voip/user-status` | [docs](https://www.yay.com/voip/api-docs/users/sip-user/) |
| [List SIP Users](actions/list-sip-users.md) | `GET /voip/user` | [docs](https://www.yay.com/voip/api-docs/users/sip-user/) |
| [List Sounds](actions/list-sounds.md) | `GET /voip/sound` | [docs](https://www.yay.com/voip/api-docs/audio/sound/) |
| [List Speed Dials](actions/list-speed-dials.md) | `GET /voip/speed-dial` | [docs](https://www.yay.com/voip/api-docs/speed-dial/speed-dial/) |
| [List Storefronts](actions/list-storefronts.md) | `GET /account/store` | [docs](https://www.yay.com/voip/api-docs/account/account-store/) |
| [List Sub Resellers](actions/list-sub-resellers.md) | `GET /account/reseller` | [docs](https://www.yay.com/voip/api-docs/account/account-sub-reseller/) |
| [List Time Diaries](actions/list-time-diaries.md) | `GET /voip/out-of-hours` | [docs](https://www.yay.com/voip/api-docs/numbers/diary/) |
| [List VoIP Trunks](actions/list-voip-trunks.md) | `GET /voip/trunk` | [docs](https://www.yay.com/voip/api-docs/trunks/trunk/) |
