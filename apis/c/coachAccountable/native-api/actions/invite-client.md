# Invite Client with CoachAccountable

Sends a client invite in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Invite Client](https://www.coachaccountable.com/APIDocs#Client.invite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `inviteSubject` | body | `string` | no | Subject line of the invite email to be sent. If not included, will use template setting. |
| `inviteMessage` | body | `string` | no | Body of the invite email to be sent, [magicLink] is required. If not included, will use template setting. |
