# Enrich Input with MailRook Email Validation

Retrieves enrichment data from MailRook for an email or domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/enrich/:input`
- **Base URL:** `https://api.mailrook.com/v1`
- **Official documentation:** [Enrich Input](https://mailrook.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | path | `string` | yes | Email address or domain to enrich. |
