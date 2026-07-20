# List Applications with ironSource

Lists applications in ironSource.

## Endpoint

- **Method:** `GET`
- **Path:** `partners/publisher/applications/v6`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [List Applications](https://docs.unity.com/en-us/grow/levelplay/platform/api/application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appStatus` | query | `string` | no | Filter applications by activation status, such as active or archived. |
| `platform` | query | `string` | no | Filter applications by operating system: iOS or Android. |
