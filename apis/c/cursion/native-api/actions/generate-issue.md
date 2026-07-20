# Generate Issue with Cursion

Generates an issue from trigger data in Cursion.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/generate`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Generate Issue](https://docs.cursion.dev/api/issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The trigger resource ID. |
| `trigger` | body | `string` | yes | The trigger type: scan, test, or caserun. |
