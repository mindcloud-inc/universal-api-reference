# Create Production with Auphonic

Creates a new production in Auphonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/productions.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [Create Production](https://auphonic.com/help/api/details.html#create-a-production-with-detailed-audio-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preset` | body | `string` | yes | Preset UUID or preset name to use as the production template. |
| `input_file` | body | `string` | no | HTTP URL or external-service filename for the input media. |
| `action` | body | `list` | no | Set to start to process the production immediately. Accepted values: `start`. |
| `is_multitrack` | body | `boolean` | no | Create the production as multitrack. |
