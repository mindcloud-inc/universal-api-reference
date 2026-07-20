# Confirm a verification by its ID with Routee

Confirms a verification by its ID in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/2step/:trackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Confirm a verification by its ID](https://docs.routee.net/reference/confirm-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingId` | path | `string` | yes | the tracking id of the verification. |
| `answer` | body | `number` | yes | The answer of the verification. |
