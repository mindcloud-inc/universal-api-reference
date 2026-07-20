# Get Latest Consent for Subject with iubenda

Retrieves the latest consent for a subject from iubenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/beta/subjects/:id/consent/last`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [Get Latest Consent for Subject](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#consent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the subject whose latest consent should be returned |
