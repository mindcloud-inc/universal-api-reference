# Publish Experiment with Zoho PageSense

Publishes an experiment in Zoho PageSense.

## Endpoint

- **Method:** `PUT`
- **Path:** `/portal/:portalName/experiments/:experimentLinkname/publish`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Publish Experiment](https://www.zoho.com/pagesense/developerguide/apidocs/publishexpts.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `experimentLinkname` | path | `string` | yes | Experiment linkname in the path. |
