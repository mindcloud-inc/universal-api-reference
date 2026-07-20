# Get user initials with Appwrite

Retrieves a user initials avatar from Appwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/avatars/initials`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get user initials](https://appwrite.io/docs/references/cloud/server-rest/avatars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Full Name. When empty, current user name or email will be used. Max length: 128 chars. |
| `width` | query | `number` | no | Image width. Pass an integer between 0 to 2000. Defaults to 100. |
| `height` | query | `number` | no | Image height. Pass an integer between 0 to 2000. Defaults to 100. |
| `background` | query | `string` | no | Changes background color. By default a random color will be picked and stay will persistent to the given name. |
