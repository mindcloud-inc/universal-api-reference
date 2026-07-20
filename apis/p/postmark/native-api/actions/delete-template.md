# Delete Template with Postmark

Deletes a template from Postmark.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/templates/:templateIdOrAlias`
- **Base URL:** `https://api.postmarkapp.com`
- **Official documentation:** [Delete Template](https://postmarkapp.com/developer/api/templates-api#delete-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateIdOrAlias` | path | `string` | yes | The Postmark template ID or alias. |
