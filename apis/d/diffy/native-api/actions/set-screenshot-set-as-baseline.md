# Set Screenshot Set as Baseline with Diffy

Sets a screenshot set as baseline in Diffy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id/set-base-line-set/:screenshot_id`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Set Screenshot Set as Baseline](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project ID. |
| `screenshot_id` | path | `number` | yes | Screenshot ID. |
