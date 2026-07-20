# Invite Styleguide Member with Zeplin

Invites a member to a Zeplin styleguide.

## Endpoint

- **Method:** `POST`
- **Path:** `/styleguides/{styleguide_id}/members`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Invite Styleguide Member](https://docs.zeplin.dev/reference/invitestyleguidemember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `handle` | body | `string` | yes | Email, username or unique identifier of the user Can also be `"me"` for joining the styleguide as the current user |
