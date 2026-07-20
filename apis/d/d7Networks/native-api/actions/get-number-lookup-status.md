# Get Number Lookup Status with D7 Networks

Retrieves number lookup status from D7 Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/hlr/v1/report/:requestId`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get Number Lookup Status](https://d7networks.com/docs/number-lookup/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Request ID returned by the D7 Number Lookup endpoint. |
