# Check Verification Status with Routee

Retrieves the verification status from Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/telegram/checkVerificationStatus`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Check Verification Status](https://docs.routee.net/reference/check-verification-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | body | `string` | yes | Unique identifier from the checkSendAbility method |
| `code` | body | `string` | no | The code entered by the user. If provided, the method checks if the code is valid for the relevant request |
