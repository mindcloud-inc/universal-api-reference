# Invite Event Managers with WaiverFile

Invites event managers to an event in WaiverFile.

## Endpoint

- **Method:** `POST`
- **Path:** `/InviteEventManagers`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [Invite Event Managers](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventID` | query | `string` | yes |
| `emailAddresses` | query | `string` | yes |
| `managerEmailMessage` | query | `string` | yes |
| `skipSendingEmailIfAccountExists` | query | `boolean` | yes |
