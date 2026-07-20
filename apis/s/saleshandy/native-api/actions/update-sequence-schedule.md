# Update Sequence Schedule with Saleshandy

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sequences/[:sequenceId]/schedule`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [Update Sequence Schedule](https://developer.saleshandy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sequenceId` | path | `string` | yes | Sequence ID to update. |
| `scheduleId` | body | `string` | yes | Schedule ID to assign to the sequence. |
