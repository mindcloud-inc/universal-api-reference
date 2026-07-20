# Update Goal for Experiment with Zoho PageSense

Updates an experiment goal in Zoho PageSense.

## Endpoint

- **Method:** `PUT`
- **Path:** `/portal/:portalName/goals/:goalLinkname`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Update Goal for Experiment](https://www.zoho.com/pagesense/developerguide/apidocs/updategoalsabsplittest.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `goalLinkname` | path | `string` | yes | Goal linkname in the path. |
| `goal.display_name` | body | `string` | no | Updated goal display name. |
| `goal.project_linkname` | body | `string` | yes | Project linkname for the goal. |
| `goal.experiment_linkname` | body | `string` | yes | Experiment linkname for the goal. |
