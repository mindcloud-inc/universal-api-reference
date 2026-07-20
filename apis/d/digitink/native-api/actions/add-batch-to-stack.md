# Add Batch To Stack with Digit.ink

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stackUuid`
- **Base URL:** `https://app.digit.ink/api/v1`
- **Official documentation:** [Add Batch To Stack](https://app.digit.ink/api/v1/classic-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackUuid` | path | `string` | yes | Stack UUID path parameter. |
| `batchUuid` | body | `string` | no | Batch UUID to add to the stack. |
| `issued` | body | `string` | no | Issued timestamp to identify the batch to add. |
