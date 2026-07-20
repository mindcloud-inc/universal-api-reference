# Get Appointment with Alto

Retrieves an appointment from Alto by ID and instance.

## Endpoint

- **Method:** `GET`
- **Path:** `/appointments/:appointmentId/:instanceId`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Appointment](https://developers.vebraalto.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointmentId` | path | `string` | yes | Unique Alto appointment identifier. |
| `instanceId` | path | `number` | yes | Numeric appointment instance identifier. |
