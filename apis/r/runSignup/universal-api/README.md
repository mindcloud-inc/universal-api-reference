# <img src="https://images.mindcloud.co/apps/icons/run-signup_1773939854144.png" alt="RunSignup logo" width="28" height="28"> RunSignup: Universal API

RunSignup is a race-registration and event-operations platform with APIs for race data, participants, results, fundraising, and related race-management workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/runSignup/latest
- **Category:** Support / Ticketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://runsignup.com
- **Vendor API docs:** https://runsignup.com/API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Races](actions/list-races.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-races?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bib Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Bib and Chip Numbers](actions/assign-bib-and-chip-numbers.md) | PUT |  |
| [List Bib and Chip Numbers](actions/list-bib-and-chip-numbers.md) | GET |  |

### Bib Validation Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Bib Validation Settings](actions/get-bib-validation-settings.md) | GET |  |

### Corporate Team

| Action | Method | Description |
| --- | --- | --- |
| [List Corporate Teams](actions/list-corporate-teams.md) | GET |  |

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Add or Edit Coupon](actions/add-or-edit-coupon.md) | PUT |  |
| [List Coupons](actions/list-coupons.md) | GET |  |

### Event Result

| Action | Method | Description |
| --- | --- | --- |
| [List Event Results](actions/list-event-results.md) | GET |  |

### Event Result Set

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Result Set](actions/create-event-result-set.md) | POST |  |
| [Edit Event Result Set](actions/edit-event-result-set.md) | PUT |  |
| [List Event Result Sets](actions/list-event-result-sets.md) | GET |  |

### Event Start Time

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Start Time](actions/get-event-start-time.md) | GET |  |

### Event Transfer Registration

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Active Registration ID for Event Transfers](actions/get-current-active-registration-id-for-event-transfers.md) | GET |  |

### Race

| Action | Method | Description |
| --- | --- | --- |
| [Get Race](actions/get-race.md) | GET |  |
| [List Races](actions/list-races.md) | GET |  |

### Race Corral

| Action | Method | Description |
| --- | --- | --- |
| [Create or Edit Race Corrals](actions/create-or-edit-race-corrals.md) | PUT |  |
| [Delete Race Corrals](actions/delete-race-corrals.md) | DELETE |  |
| [List Race Corrals](actions/list-race-corrals.md) | GET |  |

### Race Description

| Action | Method | Description |
| --- | --- | --- |
| [Set Race Description](actions/set-race-description.md) | PUT |  |

### Race Division

| Action | Method | Description |
| --- | --- | --- |
| [Create or Edit Race Divisions](actions/create-or-edit-race-divisions.md) | PUT |  |
| [Delete Race Divisions](actions/delete-race-divisions.md) | DELETE |  |
| [List Race Divisions](actions/list-race-divisions.md) | GET |  |

### Race Division Grouping

| Action | Method | Description |
| --- | --- | --- |
| [List Race Division Groupings](actions/list-race-division-groupings.md) | GET |  |

### Race Donation

| Action | Method | Description |
| --- | --- | --- |
| [List Race Donations](actions/list-race-donations.md) | GET |  |

### Race Fundraiser

| Action | Method | Description |
| --- | --- | --- |
| [List Race Fundraisers](actions/list-race-fundraisers.md) | GET |  |

### Race Participant

| Action | Method | Description |
| --- | --- | --- |
| [Add or Edit Race Participants](actions/add-or-edit-race-participants.md) | PUT |  |
| [Delete Participants](actions/delete-participants.md) | DELETE |  |
| [List Race Participants](actions/list-race-participants.md) | GET |  |

### Race Participant Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Race Participant Counts](actions/get-race-participant-counts.md) | GET |  |

### Race Participant Event

| Action | Method | Description |
| --- | --- | --- |
| [Switch Participant Events](actions/switch-participant-events.md) | PUT |  |

### Race Sync Setting

| Action | Method | Description |
| --- | --- | --- |
| [Update Race Syncing Settings](actions/update-race-syncing-settings.md) | PUT |  |

### Race Team

| Action | Method | Description |
| --- | --- | --- |
| [Add or Edit Race Groups and Teams](actions/add-or-edit-race-groups-and-teams.md) | PUT |  |
| [Create or Edit Race Teams](actions/create-or-edit-race-teams.md) | PUT |  |
| [List Race Groups and Teams](actions/list-race-groups-and-teams.md) | GET |  |

### Race Team Type

| Action | Method | Description |
| --- | --- | --- |
| [List Race Group and Team Types](actions/list-race-group-and-team-types.md) | GET |  |
| [Manage Race Group and Team Types](actions/manage-race-group-and-team-types.md) | PUT |  |

### Race Theme

| Action | Method | Description |
| --- | --- | --- |
| [Get Race Theme](actions/get-race-theme.md) | GET |  |

### Race Url

| Action | Method | Description |
| --- | --- | --- |
| [Set Race URLs](actions/set-race-urls.md) | PUT |  |

### Removed Race Participant

| Action | Method | Description |
| --- | --- | --- |
| [List Removed Race Participants](actions/list-removed-race-participants.md) | GET |  |

### Timing Data

| Action | Method | Description |
| --- | --- | --- |
| [List Timing Data](actions/list-timing-data.md) | GET |  |

### Waiver Signature

| Action | Method | Description |
| --- | --- | --- |
| [Sign Waivers](actions/sign-waivers.md) | POST |  |

