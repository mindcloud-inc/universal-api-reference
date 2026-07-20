# Add Contact Note with Salesmate

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/v4/modules/1/object/:contactId/notes`
- **Base URL:** `https://apis.salesmate.io`
- **Official documentation:** [Add Contact Note](https://apidocs.salesmate.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Salesmate contact ID. |
| `note` | body | `string` | yes | Note body in HTML or rich text markup. |
