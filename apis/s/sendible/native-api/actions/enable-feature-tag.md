# Enable Feature Tag with Sendible

## Endpoint

- **Method:** `POST`
- **Path:** `api/v2/features`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Enable Feature Tag](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureTagId` | body | `number` | yes | Feature tag ID to enable. |
| `target` | body | `string` | no | Feature target scope. |
