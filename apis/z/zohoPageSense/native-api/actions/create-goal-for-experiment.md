# Create Goal for Experiment with Zoho PageSense

Creates an experiment goal in Zoho PageSense.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/:portalName/goals`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Create Goal for Experiment](https://www.zoho.com/pagesense/developerguide/apidocs/creategoalsabsplittest.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `goal.display_name` | body | `string` | yes | Human-readable goal name. |
| `goal.goal_type` | body | `number` | yes | Goal type code from Zoho PageSense. |
| `goal.project_linkname` | body | `string` | yes | Project linkname for the goal. |
| `goal.experiment_linkname` | body | `string` | yes | Experiment linkname for the goal. |
