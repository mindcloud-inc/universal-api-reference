# Create Bulk Submissions with FillFaster

Creates multiple submissions in FillFaster.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/submission/createBulkSubmissions`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Create Bulk Submissions](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#7df8f71d-2da7-4e4b-bc71-6300c6916d14)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissions[]` | body | `array<object>` | yes | Root array of bulk submission objects. |
