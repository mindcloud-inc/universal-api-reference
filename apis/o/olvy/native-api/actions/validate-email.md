# Validate Email with Olvy

Validates an email address in Olvy.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://app.olvy.co/api/v2/graphql`
- **Official documentation:** [Validate Email](https://app.olvy.co/settings/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.email` | body | `string` | yes | Email address to validate against Olvy's checker. |
