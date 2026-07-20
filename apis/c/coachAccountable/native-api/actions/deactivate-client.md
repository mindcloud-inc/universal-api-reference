# Deactivate Client with CoachAccountable

Deactivates a client in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Deactivate Client](https://www.coachaccountable.com/APIDocs#Client.deactivate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `mayAccessWhenInactive` | body | `boolean` | no | Setting true will grant continued, read-only access to the client. |
