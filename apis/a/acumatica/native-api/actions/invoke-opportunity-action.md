# Invoke Opportunity Action with Acumatica

## Endpoint

- **Method:** `POST`
- **Path:** `/entity/:webServiceEndpoint/:endpointVersion/Opportunity/:actionName`
- **Base URL:** `{uRL}`
- **Official documentation:** [Invoke Opportunity Action](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webServiceEndpoint` | path | `string` | yes | Name of the Acumatica web service endpoint. |
| `endpointVersion` | path | `string` | yes | Version of the web service endpoint. |
| `actionName` | path | `string` | yes | Name of the opportunity action to run. |
