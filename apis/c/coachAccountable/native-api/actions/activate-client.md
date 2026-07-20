# Activate Client with CoachAccountable

Activates a client in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Activate Client](https://www.coachaccountable.com/APIDocs#Client.activate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `upgradeIfNeeded` | body | `boolean` | no | If alread at the limit, upgrade the account to make space for the newly active Client. If false, the call will return failure when there is no space. |
