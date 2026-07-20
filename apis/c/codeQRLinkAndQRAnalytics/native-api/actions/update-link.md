# Update Link with CodeQR - Link and QR Analytics

Updates a link in CodeQR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/links/:linkId`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Update Link](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkId` | path | `string` | yes | The ID of the link to update. |
| `title` | body | `string` | no | The title of the short link. |
