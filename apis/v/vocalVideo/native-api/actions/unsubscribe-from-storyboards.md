# Unsubscribe from Storyboards with Vocal Video

Deletes a storyboard webhook subscription from Vocal Video.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/storyboards/unsubscribe`
- **Base URL:** `https://vocalvideo.com/api/v1`
- **Official documentation:** [Unsubscribe from Storyboards](https://help.vocalvideo.com/article/23-using-the-subscription-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zap_id` | body | `number` | yes | Callback id returned by the subscribe action. |
