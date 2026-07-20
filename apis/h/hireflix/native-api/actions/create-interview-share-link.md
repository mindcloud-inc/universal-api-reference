# Create Interview Share Link with Hireflix

Creates a shareable interview link in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [Create Interview Share Link](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Hireflix interview ID. |
| `variables.durationInDays` | body | `number` | no | How many days the share link should remain active. |
| `variables.labels` | body | `string` | no | Optional labels to attach to the generated share link. Send multiple values as a array. |
