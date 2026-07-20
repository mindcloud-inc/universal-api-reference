# End Prediction with Twitch

Ends an existing prediction in Twitch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/predictions`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [End Prediction](https://dev.twitch.tv/docs/api/reference#end-prediction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | body | `string` | yes | The ID of the broadcaster that’s running the prediction. |
| `id` | body | `string` | yes | The ID of the prediction to update. |
| `status` | body | `string` | yes | The status to set the prediction to. Accepted values: `CANCELED`, `LOCKED`, `RESOLVED`. |
| `winning_outcome_id` | body | `string` | no | The ID of the winning outcome when resolving a prediction. |
