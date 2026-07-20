# Add Company Note with Salesmate

## Endpoint

- **Method:** `POST`
- **Path:** `/company/v4/modules/5/object/:companyId/notes`
- **Base URL:** `https://apis.salesmate.io`
- **Official documentation:** [Add Company Note](https://apidocs.salesmate.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Salesmate company ID. |
| `note` | body | `string` | yes | Note body in HTML or rich text markup. |
