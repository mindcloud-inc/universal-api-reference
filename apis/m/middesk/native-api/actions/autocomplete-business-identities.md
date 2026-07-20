# Autocomplete business identities with Middesk

Autocompletes business identities in your Middesk account.

## Endpoint

- **Method:** `POST`
- **Path:** `/identities/autocomplete`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Autocomplete business identities](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Business name to autocomplete. |
