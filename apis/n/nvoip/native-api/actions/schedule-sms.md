# Schedule SMS with Nvoip

## Endpoint

- **Method:** `POST`
- **Path:** `/sched/torpedo`
- **Base URL:** `https://api.nvoip.com.br/v2`
- **Official documentation:** [Schedule SMS](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/index.js)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | SMS message to schedule. |
| `schedulingDate` | body | `string` | yes | Date and time when the SMS should be sent. |
| `toNumber` | body | `string` | yes | Destination number for the scheduled SMS. |
