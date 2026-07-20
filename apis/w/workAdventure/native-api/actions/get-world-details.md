# Get world details with WorkAdventure

Retrieves details for a WorkAdventure world by slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/worlds/:worldSlug`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [Get world details](https://docs.workadventu.re/developer/inbound-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `worldSlug` | path | `string` | yes | The world slug from the WorkAdventure world URL, for example `mindcloud`. |
