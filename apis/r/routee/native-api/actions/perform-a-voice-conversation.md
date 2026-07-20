# Perform a voice conversation with Routee

Creates a voice conversation in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/conversation`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Perform a voice conversation](https://docs.routee.net/reference/perform-a-voice-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `object` | yes | The recipient of the call. The destination phone number. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). NOTE: limit 1 reqest per second |
| `from` | body | `string` | yes | The sender id for the call. NOTICE: Alphanumeric sender is not supported by all networks (e.g. Greek networks). Check restrictions and features here: https://go.routee.net/#/management/restrictions-and-features. |
| `dialPlan` | body | `object` | no | A combination of action verbs to be executed. Can not be empty. Use either "dialPlanUrl" or "dialPlan". |
| `dialPlanUrl` | body | `string` | no | The url which contains a combination of action verbs to be executed. Use either "dialPlanUrl" or "dialPlan". |
| `callback` | body | `object` | no | Defines the notification callback information for the progress of Voice conversation |
| `hangupDelay` | body | `number` | no | The time to wait for the call to be answered. Min value: 1.  Max value: 60. |
| `maxDuration` | body | `number` | no | Defines the maximum duration. Min value: 1 |
| `machineDetection` | body | `object` | no | It is used to detect if the call is answered by human or machine and define the desired actions (in case of machine). |
