# Fetch Blueprint with Apiary

Retrieves an API blueprint from Apiary by API name.

## Endpoint

- **Method:** `GET`
- **Path:** `/blueprint/get/{{apiName}}`
- **Base URL:** `https://api.apiary.io`
- **Official documentation:** [Fetch Blueprint](https://apiary.docs.apiary.io/reference/fetch-blueprint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apiName` | path | `string` | yes | Select the Apiary API subdomain to read blueprint source from. |
