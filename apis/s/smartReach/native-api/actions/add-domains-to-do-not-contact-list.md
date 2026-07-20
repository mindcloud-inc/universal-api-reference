# Add Domains to Do Not Contact List with SmartReach

Adds domains to the do not contact list in SmartReach.

## Endpoint

- **Method:** `POST`
- **Path:** `/do_not_contact/domain`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Add Domains to Do Not Contact List](https://help.smartreach.io/reference/adddomainstodnc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains[]` | body | `array<object>` | no | Domains to be blacklisted with an exclusion list |
