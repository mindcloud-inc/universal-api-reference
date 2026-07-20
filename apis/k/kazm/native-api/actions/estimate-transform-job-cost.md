# Estimate Transform Job Cost with Kazm

Retrieves a transform job cost estimate from Kazm.

## Endpoint

- **Method:** `POST`
- **Path:** `/transform-jobs/cost-estimation`
- **Base URL:** `https://api.lightningrod.ai/api/public/v1`
- **Official documentation:** [Estimate Transform Job Cost](https://docs.lightningrod.ai/rest-api/transform-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `config` | body | `object` | yes | Transform job configuration payload. |
