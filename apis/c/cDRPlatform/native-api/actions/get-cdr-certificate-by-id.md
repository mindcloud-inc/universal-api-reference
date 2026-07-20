# Get CDR Certificate By ID with CDR Platform

Retrieves a CDR certificate by ID from CDR Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/certificate/:id/`
- **Base URL:** `https://api.cdrplatform.com`
- **Official documentation:** [Get CDR Certificate By ID](https://api.cdrplatform.com/schema/redoc/#tag/Certificate/operation/certificate_retrieve_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Certificate ID using the documented three-part code format, for example ABC-DEF-GHI. |
