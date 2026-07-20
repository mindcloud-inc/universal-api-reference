# Create Statement Batch with GrassBlade LRS

Stores a batch of statements in GrassBlade LRS.

## Endpoint

- **Method:** `POST`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Create Statement Batch](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtrespost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statements[]` | body | `array<object>` | yes | Array of Statement objects to store in one request. |
