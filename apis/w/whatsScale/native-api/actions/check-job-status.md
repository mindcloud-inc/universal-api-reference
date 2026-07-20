# Check Job Status with WhatsScale

Retrieves an async job status from WhatsScale.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/status/:jobId`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Check Job Status](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Job ID returned by async send or story endpoints. |
