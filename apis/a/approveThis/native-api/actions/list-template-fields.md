# List Template Fields with ApproveThis

Retrieves fields for an approval template in ApproveThis.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/:template/fields`
- **Base URL:** `https://app.approvethis.com/api/v1`
- **Official documentation:** [List Template Fields](https://app.approvethis.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | path | `string` | yes | The template slug. |
