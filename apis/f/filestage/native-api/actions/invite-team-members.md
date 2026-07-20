# Invite Team Members with Filestage

Creates team member invitations in Filestage.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/members/{memberId}`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Invite Team Members](https://developers.filestage.io/docs/api/bs3ac0u9uffxk-invite-team-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | Member Id |
| `email[]` | body | `array<string>` | yes | — |
| `roleId` | body | `string` | yes | — |
