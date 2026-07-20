# Evaluate Profile with Ninetailed

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/organizations/:organizationId/environments/:environmentSlug/profiles`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Evaluate Profile](https://www.contentful.com/developers/docs/personalization/experience-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<object>` | yes | Events to evaluate for the profile request. |
| `locale` | query | `string` | no | ISO 639-1 language code used for experience evaluation. |
