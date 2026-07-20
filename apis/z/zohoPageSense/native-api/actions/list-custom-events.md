# List Custom Events with Zoho PageSense

Retrieves custom events from Zoho PageSense.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/:portalName/customevents`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [List Custom Events](https://www.zoho.com/pagesense/developerguide/apidocs/fetcheventsapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `project_linkname` | query | `string` | yes | Project linkname query parameter. |
