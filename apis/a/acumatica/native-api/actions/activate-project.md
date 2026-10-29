# Activate Project with Acumatica

Make an existing Acumatica project active by setting Hold to false.

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Project`
- **Base URL:** `{uRL}`
- **Official documentation:** [Activate Project](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Project/Make-a-Project-Active)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ProjectID` | body | `object` | no |
| `ProjectID.value` | body | `string` | yes |
