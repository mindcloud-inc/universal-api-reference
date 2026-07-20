# Get Client Diagnoses with IntakeQ

Retrieves client diagnoses from IntakeQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/client/{clientId}/diagnoses`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Get Client Diagnoses](https://support.intakeq.com/article/251-intakeq-client-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `string` | yes | The IntakeQ numeric client ID. |
