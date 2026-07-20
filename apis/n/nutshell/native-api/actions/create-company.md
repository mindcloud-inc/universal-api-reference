# Create Company with Nutshell

Creates a new company in Nutshell.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Create Company](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[].name` | body | `string` | no | Name of the company. |
| `accounts[].description` | body | `string` | no | Description of the company. |
| `accounts[].emails[].value` | body | `string` | no | Email address for the company. |
| `accounts[].phones[].value` | body | `string` | no | Phone number for the company. |
| `accounts[].urls[].value` | body | `string` | no | Website URL for the company. |
