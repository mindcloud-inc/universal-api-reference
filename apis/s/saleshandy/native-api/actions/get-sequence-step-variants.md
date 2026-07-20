# Get Sequence Step Variants with Saleshandy

## Endpoint

- **Method:** `GET`
- **Path:** `/sequences/[:sequenceId]/steps/[:stepId]`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [Get Sequence Step Variants](https://developer.saleshandy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sequenceId` | path | `string` | yes | Sequence ID that owns the step. |
| `stepId` | path | `string` | yes | Step ID to fetch variants for. |
