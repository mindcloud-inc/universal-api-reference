# RunSignup: Native API Reference

A consolidated summary of RunSignup's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://runsignup.com/API
- **API base URL:** `https://api.runsignup.com/rest`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://runsignup.com/Profile/OAuth2/RequestGrant to approve access.
2. Exchange the returned authorization code with a POST request to https://api.runsignup.com/rest/v2/auth/auth-code-redemption.json.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `rsu_api_read rsu_api_write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.runsignup.com/rest/v2/auth/refresh-token.json.

[Official authentication documentation](https://runsignup.com/API/OAuth2)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add or Edit Coupon](actions/add-or-edit-coupon.md) | `POST /race/:race_id/coupons` | [docs](https://runsignup.com/API/race/:race_id/coupons/POST) |
| [Add or Edit Race Groups and Teams](actions/add-or-edit-race-groups-and-teams.md) | `POST /race/:race_id/teams` | [docs](https://runsignup.com/API/race/:race_id/teams/POST) |
| [Add or Edit Race Participants](actions/add-or-edit-race-participants.md) | `POST /race/:race_id/participants` | [docs](https://runsignup.com/API/race/:race_id/participants/POST) |
| [Assign Bib and Chip Numbers](actions/assign-bib-and-chip-numbers.md) | `POST /race/:race_id/assign-bib-chip` | [docs](https://runsignup.com/API/race/:race_id/assign-bib-chip/POST) |
| [Create Event Result Set](actions/create-event-result-set.md) | `POST /race/:race_id/results/new-result-set` | [docs](https://runsignup.com/API/race/:race_id/results/new-result-set/POST) |
| [Create or Edit Race Corrals](actions/create-or-edit-race-corrals.md) | `POST /v2/corrals/manage-corrals.json` | [docs](https://runsignup.com/API/v2/corrals/manage-corrals.json/POST) |
| [Create or Edit Race Divisions](actions/create-or-edit-race-divisions.md) | `POST /v2/divisions/manage-divisions.json` | [docs](https://runsignup.com/API/v2/divisions/manage-divisions.json/POST) |
| [Create or Edit Race Teams](actions/create-or-edit-race-teams.md) | `POST /v2/teams/manage-teams.json` | [docs](https://runsignup.com/API/v2/teams/manage-teams.json/POST) |
| [Delete Participants](actions/delete-participants.md) | `POST /race/:race_id/delete-participants` | [docs](https://runsignup.com/API/race/:race_id/delete-participants/POST) |
| [Delete Race Corrals](actions/delete-race-corrals.md) | `POST /v2/corrals/delete-corrals.json` | [docs](https://runsignup.com/API/v2/corrals/delete-corrals.json/POST) |
| [Delete Race Divisions](actions/delete-race-divisions.md) | `POST /v2/divisions/delete-divisions.json` | [docs](https://runsignup.com/API/v2/divisions/delete-divisions.json/POST) |
| [Edit Event Result Set](actions/edit-event-result-set.md) | `POST /race/:race_id/results/edit-result-set` | [docs](https://runsignup.com/API/race/:race_id/results/edit-result-set/POST) |
| [Get Bib Validation Settings](actions/get-bib-validation-settings.md) | `GET /race/:race_id/get-bib-validation-settings` | [docs](https://runsignup.com/API/race/:race_id/get-bib-validation-settings/GET) |
| [Get Current Active Registration ID for Event Transfers](actions/get-current-active-registration-id-for-event-transfers.md) | `POST /race/:race_id/get-event-transfer-participant-final-registration` | [docs](https://runsignup.com/API/race/:race_id/get-event-transfer-participant-final-registration/POST) |
| [Get Event Start Time](actions/get-event-start-time.md) | `GET /race/:race_id/results/start-time` | [docs](https://runsignup.com/API/race/:race_id/results/start-time/GET) |
| [Get Race](actions/get-race.md) | `GET /race/:race_id` | [docs](https://runsignup.com/API/race/:race_id/GET) |
| [Get Race Participant Counts](actions/get-race-participant-counts.md) | `GET /race/:race_id/participant-counts` | [docs](https://runsignup.com/API/race/:race_id/participant-counts/GET) |
| [Get Race Theme](actions/get-race-theme.md) | `GET /v2/race-theme/race-theme.json` | [docs](https://runsignup.com/API/v2/race-theme/race-theme.json/GET) |
| [List Bib and Chip Numbers](actions/list-bib-and-chip-numbers.md) | `GET /race/:race_id/get-bib-chip` | [docs](https://runsignup.com/API/race/:race_id/get-bib-chip/GET) |
| [List Corporate Teams](actions/list-corporate-teams.md) | `GET /race/:race_id/corporate-teams` | [docs](https://runsignup.com/API/race/:race_id/corporate-teams/GET) |
| [List Coupons](actions/list-coupons.md) | `GET /race/:race_id/coupons` | [docs](https://runsignup.com/API/race/:race_id/coupons/GET) |
| [List Event Result Sets](actions/list-event-result-sets.md) | `GET /race/:race_id/results/get-result-sets` | [docs](https://runsignup.com/API/race/:race_id/results/get-result-sets/GET) |
| [List Event Results](actions/list-event-results.md) | `GET /race/:race_id/results/get-results` | [docs](https://runsignup.com/API/race/:race_id/results/get-results/GET) |
| [List Race Corrals](actions/list-race-corrals.md) | `GET /race/:race_id/corrals` | [docs](https://runsignup.com/API/race/:race_id/corrals/GET) |
| [List Race Division Groupings](actions/list-race-division-groupings.md) | `GET /race/:race_id/divisions/division-grouping` | [docs](https://runsignup.com/API/race/:race_id/divisions/division-grouping/GET) |
| [List Race Divisions](actions/list-race-divisions.md) | `GET /race/:race_id/divisions/divisions` | [docs](https://runsignup.com/API/race/:race_id/divisions/divisions/GET) |
| [List Race Donations](actions/list-race-donations.md) | `GET /race/:race_id/donations/list` | [docs](https://runsignup.com/API/race/:race_id/donations/list/GET) |
| [List Race Fundraisers](actions/list-race-fundraisers.md) | `GET /v2/race-fundraisers/get-race-fundraisers.json` | [docs](https://runsignup.com/API/v2/race-fundraisers/get-race-fundraisers.json/GET) |
| [List Race Group and Team Types](actions/list-race-group-and-team-types.md) | `GET /race/:race_id/teams/team-types` | [docs](https://runsignup.com/API/race/:race_id/teams/team-types/GET) |
| [List Race Groups and Teams](actions/list-race-groups-and-teams.md) | `GET /race/:race_id/teams` | [docs](https://runsignup.com/API/race/:race_id/teams/GET) |
| [List Race Participants](actions/list-race-participants.md) | `GET /race/:race_id/participants` | [docs](https://runsignup.com/API/race/:race_id/participants/GET) |
| [List Races](actions/list-races.md) | `GET /races` | [docs](https://runsignup.com/API/races/GET) |
| [List Removed Race Participants](actions/list-removed-race-participants.md) | `GET /race/:race_id/removed-participants` | [docs](https://runsignup.com/API/race/:race_id/removed-participants/GET) |
| [List Timing Data](actions/list-timing-data.md) | `GET /race/:race_id/results/get-timing-data` | [docs](https://runsignup.com/API/race/:race_id/results/get-timing-data/GET) |
| [Manage Race Group and Team Types](actions/manage-race-group-and-team-types.md) | `POST /race/:race_id/teams/team-types` | [docs](https://runsignup.com/API/race/:race_id/teams/team-types/POST) |
| [Set Race Description](actions/set-race-description.md) | `POST /race/:race_id/race-description` | [docs](https://runsignup.com/API/race/:race_id/race-description/POST) |
| [Set Race URLs](actions/set-race-urls.md) | `POST /race/:race_id/race-urls` | [docs](https://runsignup.com/API/race/:race_id/race-urls/POST) |
| [Sign Waivers](actions/sign-waivers.md) | `POST /v2/participants/sign-waivers.json` | [docs](https://runsignup.com/API/v2/participants/sign-waivers.json/POST) |
| [Switch Participant Events](actions/switch-participant-events.md) | `POST /race/:race_id/switch-participant-events` | [docs](https://runsignup.com/API/race/:race_id/switch-participant-events/POST) |
| [Update Race Syncing Settings](actions/update-race-syncing-settings.md) | `POST /race/:race_id/sync-settings` | [docs](https://runsignup.com/API/race/:race_id/sync-settings/POST) |
