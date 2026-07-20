# List Selected Audiences with Zoho PageSense

Retrieves selected audiences from Zoho PageSense.

## Endpoint

- **Method:** `GET`
- **Path:** `https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/audiences`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [List Selected Audiences](https://www.zoho.com/pagesense/developerguide/apidocs/selectedaudienceexpt.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `experiment_link_name` | query | `string` | yes | Experiment link name query parameter. |
