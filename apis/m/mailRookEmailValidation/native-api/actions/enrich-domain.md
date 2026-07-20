# Enrich Domain with MailRook Email Validation

Retrieves enrichment data from MailRook for a domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/enrich/:domain`
- **Base URL:** `https://api.mailrook.com/v1`
- **Official documentation:** [Enrich Domain](https://mailrook.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain to enrich. |
