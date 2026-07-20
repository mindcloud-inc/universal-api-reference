# Add Deal Note with Salesmate

## Endpoint

- **Method:** `POST`
- **Path:** `/deal/v4/modules/4/object/:dealId/notes`
- **Base URL:** `https://apis.salesmate.io`
- **Official documentation:** [Add Deal Note](https://apidocs.salesmate.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dealId` | path | `number` | yes | Salesmate deal ID. |
| `note` | body | `string` | yes | Note body in HTML or rich text markup. |
