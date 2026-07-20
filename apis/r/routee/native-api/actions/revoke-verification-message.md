# Revoke Verification Message with Routee

Revokes a verification message in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/telegram/revokeVerificationMessage`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Revoke Verification Message](https://docs.routee.net/reference/revoke-verification-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | body | `string` | no | Unique identifier from the checkSendAbility method |
