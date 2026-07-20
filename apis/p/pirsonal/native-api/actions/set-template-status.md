# Set Template Status with Pirsonal

Updates the status of an existing template in Pirsonal.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Set Template Status](https://app.pirsonal.com/docAPI#Template_SetStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateID` | body | `string` | yes | ID of the template whose status should change. |
| `status` | body | `list<string>` | yes | Template status: active or inactive. Accepted values: `active`, `inactive`. |
