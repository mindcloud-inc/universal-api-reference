# Create Batch Validation Job with mails.so

Creates a new batch validation job in mails.so.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch`
- **Base URL:** `https://api.mails.so/v1`
- **Official documentation:** [Create Batch Validation Job](https://docs.mails.so/bulk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to validate in this batch |
