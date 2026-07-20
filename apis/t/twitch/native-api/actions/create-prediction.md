# Create Prediction with Twitch

Creates a new prediction in Twitch.

## Endpoint

- **Method:** `POST`
- **Path:** `/predictions`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Create Prediction](https://dev.twitch.tv/docs/api/reference#create-prediction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | body | `string` | yes | The ID of the broadcaster that’s running the prediction. |
| `title` | body | `string` | yes | The question that the broadcaster is asking. |
| `outcomes[].title` | body | `string` | yes | The text of one of the prediction outcomes. Send multiple values as a array. |
| `prediction_window` | body | `number` | yes | The length of time, in seconds, that the prediction will run. |
