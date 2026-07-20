# Start Programmatic Process with Landingi

Starts a programmatic landing page process in Landingi.

## Endpoint

- **Method:** `POST`
- **Path:** `/landing-page/programmatic/start`
- **Base URL:** `https://api.landingi.com/v2`
- **Official documentation:** [Start Programmatic Process](https://api.landingi.com/v2/docs#tag/programmatic-lp/operation/startProgrammaticLandingPageProcess)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceLandingPageUuid` | body | `string` | yes | UUID of the source landing page. |
| `name` | body | `string` | yes | Name of the process. |
| `immediatePublication` | body | `boolean` | yes | Whether to publish the landing pages immediately. |
| `destinationGroupName` | body | `string` | no | Name of the group to assign the landing pages to. |
| `variants[]` | body | `array<object>` | yes | Programmatic landing page data. |
| `variants[].name` | body | `string` | no | Name of the programmatic landing page. |
| `variants[].domainUrl` | body | `string` | no | Full domain URL of the landing page. |
| `variants[].placeholders[]` | body | `array<object>` | no | Placeholder values for the landing page. |
| `variants[].placeholders[].key` | body | `string` | no | Placeholder content key. |
| `variants[].placeholders[].value` | body | `string` | no | Value used to replace the placeholder. |
