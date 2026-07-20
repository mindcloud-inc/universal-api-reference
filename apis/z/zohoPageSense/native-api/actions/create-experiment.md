# Create Experiment with Zoho PageSense

Creates an experiment in Zoho PageSense.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/:portalName/experiments`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Create Experiment](https://www.zoho.com/pagesense/developerguide/apidocs/createabsplittest.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `experiment.display_name` | body | `string` | yes | Human-readable experiment name. |
| `experiment.experiment_url` | body | `string` | yes | URL included in the experiment configuration. |
| `experiment.experiment_type` | body | `number` | yes | Experiment type code from Zoho PageSense. |
| `experiment.project_linkname` | body | `string` | yes | Project linkname for the experiment. |
