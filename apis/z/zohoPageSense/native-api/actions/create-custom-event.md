# Create Custom Event with Zoho PageSense

Creates a custom event in Zoho PageSense.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/:portalName/customevents`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Create Custom Event](https://www.zoho.com/pagesense/developerguide/apidocs/createeventsapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `customevent.event_name` | body | `string` | yes | Human-friendly custom event name. |
| `customevent.project_linkname` | body | `string` | yes | Project linkname for the custom event. |
