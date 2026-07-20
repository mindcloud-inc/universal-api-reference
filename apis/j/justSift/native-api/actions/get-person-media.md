# Get Person Media with JustSift

## Endpoint

- **Method:** `GET`
- **Path:** `/media/people/:idOrEmail/:mediaKind`
- **Base URL:** `https://api.justsift.com/v1`
- **Official documentation:** [Get Person Media](https://developers.justsift.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `image/jpeg` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrEmail` | path | `string` | yes | The person's Sift id or email address. |
| `mediaKind` | path | `string` | yes | Media kind to retrieve: profile-photo or background-photo. Accepted values: `0`, `1`. |
| `preferredType` | query | `string` | no | Optional profile photo subtype preference: custom or official. Accepted values: `0`, `1`. |
| `height` | query | `number` | no | Image height to return, up to 1000. |
| `width` | query | `number` | no | Image width to return, up to 1000. |
| `fit` | query | `string` | no | Image fit mode: crop or scale. Accepted values: `0`, `1`. |
