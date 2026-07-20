# HLR Check with LabsMobile

Checks mobile number status and availability with LabsMobile HLR lookup.

## Endpoint

- **Method:** `GET`
- **Path:** `/hlr`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [HLR Check](https://www.labsmobile.com/en/sms-api/api-versions/hlr-check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numbers` | query | `string` | yes | One or more comma-separated phone numbers in E.164 format. |
| `type` | query | `string` | no | HLR check type such as status, network, or format. |
