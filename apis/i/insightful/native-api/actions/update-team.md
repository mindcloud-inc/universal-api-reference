# Update Team with Insightful

Updates an existing team in your Insightful account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/team/:id`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Update Team](https://developers.insightful.io/#dab41be7-d81a-46fc-8903-5120f8d15b42)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The updated team description. |
| `employees[]` | body | `array<string>` | no | Employee IDs to assign to the team. |
| `id` | path | `string` | yes | The team ID to update. |
| `ignoreNeutral` | body | `boolean` | no | Whether to ignore neutral applications for the team. |
| `ignoreProductive` | body | `boolean` | no | Whether to ignore productive applications for the team. |
| `ignoreUnproductive` | body | `boolean` | no | Whether to ignore unproductive applications for the team. |
| `ignoreUnreviewed` | body | `boolean` | no | Whether to ignore unreviewed applications for the team. |
| `projects[]` | body | `array<string>` | no | Project IDs to assign to the team. |
