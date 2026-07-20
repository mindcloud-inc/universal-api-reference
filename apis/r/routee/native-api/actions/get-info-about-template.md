# Get info about template with Routee

Retrieves info about template from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/template/:templateId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Get info about template](https://docs.routee.net/reference/get-info-about-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | ID of the template uploaded in the service. Use this method to get the template ID (use either real_id or id parameter from the reply) |
