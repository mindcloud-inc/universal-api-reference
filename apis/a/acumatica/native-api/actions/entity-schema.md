# Get Entity Schema with Acumatica

Get a specific Entity schema from the 'Default' Acumatica Endpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/Default/:endpointVersion/:entity/$adHocSchema`
- **Base URL:** `{uRL}`
- **Official documentation:** [Get Entity Schema](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | path | `list<string>` | yes | The top-level entity to retrieve. Example: "Project" or "User" Accepted values: `ProFormaInvoice`, `Project`, `ProjectBudget`, `ProjectTask`, `SalesOrder`. |
| `endpointVersion` | path | `list<string>` | yes | — |
