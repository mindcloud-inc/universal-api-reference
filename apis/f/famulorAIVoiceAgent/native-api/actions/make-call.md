# Make a Call with Famulor AI - Voice Agent

Creates a new call in Famulor with a specific assistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/make_call`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Make a Call](https://docs.famulor.io/en/api-reference/calls/make)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | body | `number` | yes | Assistant ID that will handle the call. |
| `phone_number` | body | `string` | yes | Destination phone number in E.164 format. |
| `variables` | body | `object` | no | Optional dynamic variables for call personalization. |
