# List Acumatica Endpoints with Acumatica

Retrieve the Acumatica ERP Endpoints and the build version.

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/`
- **Base URL:** `{uRL}`
- **Official documentation:** [List Acumatica Endpoints](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=1a9d6f7e-8546-426b-b1ff-d712fbcfbc7b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unusedParam` | path | `list<string>` | no | Choose what data to retrieve in the response. Accepted values are 'version' (to retrieve the Acumatica ERP version) and 'endpoints' to retrieve the endpoints. |
