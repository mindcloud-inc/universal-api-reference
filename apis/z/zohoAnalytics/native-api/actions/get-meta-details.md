# Get Meta Details with Zoho Analytics

Retrieves workspace or view details from Zoho Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/metadetails`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Get Meta Details](https://raw.githubusercontent.com/zoho/analytics-oas/main/v2.0/metadata-api.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CONFIG` | query | `string` | yes | Stringified JSON config that identifies the target workspace or view by name, such as workspaceName, folderName, or viewName. |
