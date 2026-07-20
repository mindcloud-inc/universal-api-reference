# Check PACER Account Filer Status with Court Drive

## Endpoint

- **Method:** `POST`
- **Path:** `/pacer/credentials/check-filer-status`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Check PACER Account Filer Status](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pacer_user` | body | `string` | yes | PACER username to check filer status for. |
