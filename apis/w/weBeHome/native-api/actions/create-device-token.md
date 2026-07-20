# Create Device Token with WeBeHome

## Endpoint

- **Method:** `POST`
- **Path:** `OpenAPIservice.svc/CreateWebTokens/CreateDevice`
- **Base URL:** `https://webehome.com/API`
- **Official documentation:** [Create Device Token](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DeviceName` | body | `string` | yes | Name of the client device. |
| `LanguageID` | body | `string` | yes | Language identifier. |
