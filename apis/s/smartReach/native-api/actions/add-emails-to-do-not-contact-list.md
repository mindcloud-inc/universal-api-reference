# Add Emails to Do Not Contact List with SmartReach

Adds emails to the do not contact list in SmartReach.

## Endpoint

- **Method:** `POST`
- **Path:** `/do_not_contact/email`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Add Emails to Do Not Contact List](https://help.smartreach.io/reference/addemailstodnc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | no | Emails to be blacklisted |
