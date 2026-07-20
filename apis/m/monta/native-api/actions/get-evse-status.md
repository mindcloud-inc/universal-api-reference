# Get EVSE Status with Monta

Retrieves dynamic EVSE status from Monta.

## Endpoint

- **Method:** `GET`
- **Path:** `/afir/charge-points/{evseId}/status`
- **Base URL:** `https://public-api.monta.com/api/v1`
- **Official documentation:** [Get EVSE Status](https://docs.public-api.monta.com/reference/get-afir-evse-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `evseId` | path | `string` | yes | OCPI EVSE identifier, for example DK*MON*E100001. |
