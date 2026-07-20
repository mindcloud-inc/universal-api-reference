# Update Company with Cloze

Updates a company in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/companies/update`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Update Company](https://api.cloze.com/api-docs/#/paths/v1-companies-update/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direct` | body | `string` | no | Direct identifier for the company to update. |
| `domains[]` | body | `array<string>` | no | Domain names for the company. |
| `name` | body | `string` | yes | Name of the company. |
| `stage` | body | `list<string>` | no | Stage of the company. Accepted values: `current`, `future`, `lead`, `out`, `past`. |
