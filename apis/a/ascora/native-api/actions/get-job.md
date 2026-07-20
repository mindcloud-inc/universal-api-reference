# Get Job with Ascora

Retrieves a job from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Jobs/Job/{{jobNumber}}`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Get Job](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=49)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobNumber` | path | `string` | yes | Full job number to retrieve. |
