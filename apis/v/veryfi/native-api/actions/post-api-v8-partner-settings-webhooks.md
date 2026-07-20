# Add a webhook with Veryfi

Creates a new webhook in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/settings/webhooks`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Add a webhook](https://docs.veryfi.com/api/settings/add-a-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Possible values: non-empty and <= 2083 characters |
