# Create Dashboard with Datadog

Creates a new dashboard in Datadog.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/dashboard`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Create Dashboard](https://docs.datadoghq.com/api/latest/dashboards/#create-a-new-dashboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the dashboard. |
| `layout_type` | body | `string` | yes | Layout type of the dashboard. |
| `widgets[]` | body | `array<object>` | yes | List of widgets to display on the dashboard. |
| `description` | body | `string` | no | Description of the dashboard. |
| `notify_list[]` | body | `array<string>` | no | Handles of users to notify when changes are made to this dashboard. |
| `reflow_type` | body | `string` | no | Reflow type for ordered dashboards. |
| `restricted_roles[]` | body | `array<string>` | no | Role identifiers that can edit this dashboard. |
| `tags[]` | body | `array<string>` | no | Team tags representing dashboard ownership. |
| `template_variables[]` | body | `array<object>` | no | Template variables for this dashboard. |
| `template_variable_presets[]` | body | `array<object>` | no | Saved views for this dashboard's template variables. |
