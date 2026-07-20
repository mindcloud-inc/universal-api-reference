# Enrich Email with MailRook Email Validation

Retrieves enrichment data from MailRook for an email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/enrich/:email`
- **Base URL:** `https://api.mailrook.com/v1`
- **Official documentation:** [Enrich Email](https://mailrook.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Email address to enrich. |
