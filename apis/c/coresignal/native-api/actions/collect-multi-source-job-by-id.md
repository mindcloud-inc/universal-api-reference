# Collect Multi-source Job By ID with Coresignal

Collects a multi-source job from Coresignal by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/job_multi_source/collect/:jobId`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Collect Multi-source Job By ID](https://docs.coresignal.com/job-api/multi-source-job-api/endpoints/collect-job)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobId` | path | `number` | yes |
