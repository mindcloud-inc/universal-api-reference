# Create Submission Link with FillFaster

Creates a unique submission link in FillFaster.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/createSubmission`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Create Submission Link](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#a9ea4e58-0474-45e3-ba68-3e46b387fb9d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fid` | body | `string` | yes | Form template identifier. |
| `prefill_data` | body | `object` | no | Field values to prefill into the generated submission link. |
| `user_data` | body | `object` | no | Opaque metadata returned back in FillFaster webhooks. |
