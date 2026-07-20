# Update Form Settings with FillFaster

Updates settings for an existing form in FillFaster.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/form/update-settings`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Update Form Settings](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | body | `string` | yes | FillFaster form identifier to update. |
| `settings` | body | `object` | yes | Form settings payload. |
