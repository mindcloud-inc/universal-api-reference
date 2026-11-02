# Get Celebration Template Image Download URL with BambooHR

Retrieves celebration template image download url from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/community/recognition/settings/celebrations/:celebrationType/template-images/:fileId/download-url`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Celebration Template Image Download URL](https://documentation.bamboohr.com/reference/get-celebration-template-image-download-url)

## Requirements

- **OAuth scopes:** `recognitions:manage`
- **scope:** `recognitions:manage` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `celebrationType` | path | `list<string>` | yes | The celebration template containing the image Accepted values: `anniversary`, `birthday`. |
| `fileId` | path | `string` | yes | The Files API V2 fileId on an image node in the selected template |
