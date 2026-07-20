# Create Movie with Bannerbear

Creates a new movie in Bannerbear.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/movies`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Create Movie](https://developers.bannerbear.com/v2/#create-a-movie)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | body | `number` | yes | The desired width of your movie. |
| `height` | body | `number` | yes | The desired height of your movie. |
| `inputs[]` | body | `array<object>` | yes | A list of videos or images you want to combine into a movie. |
| `inputs[].asset_url` | body | `string` | no | URL to a video file or static image. |
| `inputs[].trim_to_length_in_seconds` | body | `number` | no | Force trim the end video to a specific time. |
| `inputs[].mute` | body | `boolean` | no | Remove the sound from this video clip. |
| `inputs[].soundtrack_url` | body | `string` | no | URL to an audio file to overlay on top of this clip. |
| `transition` | body | `string` | no | The name of the transition to use between video clips. |
| `soundtrack_url` | body | `string` | no | URL to an audio file to overlay on top of the movie. |
| `webhook_url` | body | `string` | no | A URL to POST the full Movie object to upon rendering completion. |
| `metadata` | body | `string` | no | Any metadata that you need to store, for example a record ID. |
