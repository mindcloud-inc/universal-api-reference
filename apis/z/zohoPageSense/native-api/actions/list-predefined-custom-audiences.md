# List Predefined & Custom Audiences with Zoho PageSense

Retrieves predefined and custom audiences from Zoho PageSense.

## Endpoint

- **Method:** `GET`
- **Path:** `https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/audiences`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [List Predefined & Custom Audiences](https://www.zoho.com/pagesense/developerguide/apidocs/audienceabsplittest.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `experiment_link_name` | query | `string` | yes | Experiment link name query parameter. |
| `project_link_name` | query | `string` | yes | Project link name query parameter. |
