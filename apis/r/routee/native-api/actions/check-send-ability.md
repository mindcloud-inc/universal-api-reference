# Check Send Ability with Routee

Retrieves your Routee send ability status.

## Endpoint

- **Method:** `POST`
- **Path:** `/telegram/checkSendAbility`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Check Send Ability](https://docs.routee.net/reference/check-send-ability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | body | `string` | yes | The phone number in E.164 format (e.g., `+306974444444`). |
