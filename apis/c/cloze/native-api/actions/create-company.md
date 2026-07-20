# Create Company with Cloze

Creates a company in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/companies/create`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Create Company](https://api.cloze.com/api-docs/#/paths/v1-companies-create/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description of the company |
| `domains[]` | body | `array<string>` | no | Array of domain names |
| `dryrun` | body | `boolean` | no | Run validation without creating or updating the record |
| `name` | body | `string` | no | Name of the company |
| `segment` | body | `string` | no | Segment of the company |
| `stage` | body | `list<string>` | no | Stage of the company Accepted values: `current`, `future`, `lead`, `out`, `past`. |
