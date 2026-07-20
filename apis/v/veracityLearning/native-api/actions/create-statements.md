# Create Statements with Veracity Learning

Creates one or more statements in Veracity Learning.

## Endpoint

- **Method:** `POST`
- **Path:** `/statements`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Create Statements](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statements[]` | body | `array<object>` | yes | Array of xAPI Statement objects to create. |
