# Create Fundraiser with Every.org

Creates a new fundraiser in Every.org.

## Endpoint

- **Method:** `POST`
- **Path:** `/fundraiser`
- **Base URL:** `https://partners.every.org/v0.2`
- **Official documentation:** [Create Fundraiser](https://docs.every.org/docs/endpoints/fundraisers#post-v02fundraiser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nonprofitId` | body | `string` | yes | UUID of the nonprofit supported by the fundraiser. |
| `title` | body | `string` | yes | Fundraiser title. |
| `description` | body | `string` | yes | Fundraiser description or null. |
| `goal` | body | `number` | yes | Goal amount in cents or null. |
| `raisedOffline` | body | `number` | yes | Amount raised offline in cents or null. |
| `startDate` | body | `string` | yes | ISO-encoded datetime string for when the fundraiser starts or null. |
| `endDate` | body | `string` | yes | ISO-encoded datetime string for when the fundraiser ends or null. |
| `imageBase64` | body | `string` | no | Optional base64-encoded fundraiser cover image. |
