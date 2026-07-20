# Job Change Detection with Datagma

Retrieves job change details from Datagma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/update`
- **Base URL:** `https://gateway.datagma.net/api/ingress`
- **Official documentation:** [Job Change Detection](https://datagmaapi.readme.io/reference/ingressservice_stellaupdatev2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | query | `string` | no | Target company name. |
| `debug` | query | `string` | no | Set false to allow broader scoring results. |
| `email` | query | `string` | no | Email address used as a high-certainty input for job change detection. |
| `fullName` | query | `string` | no | Target person's full name. |
| `linkedInUrl` | query | `string` | no | LinkedIn profile URL used for higher-certainty job change detection. |
