# Invite Candidate To Interview with Hireflix

Invites a candidate to an interview in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [Invite Candidate To Interview](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.positionId` | body | `string` | yes | The Hireflix position ID. |
| `variables.input.candidate.firstName` | body | `string` | yes | The candidate's first name. |
| `variables.input.candidate.lastName` | body | `string` | no | The candidate's last name. |
| `variables.input.candidate.email` | body | `string` | yes | The candidate's email address. |
| `variables.input.candidate.phone` | body | `string` | no | The candidate's phone number. |
| `variables.input.externalId` | body | `string` | no | An external ID to associate with the interview. |
| `variables.input.disableNotifications` | body | `boolean` | no | Whether to suppress Hireflix notifications for this invite. |
| `variables.input.metadata` | body | `object` | no | Optional JSON metadata to store with the interview invite. |
