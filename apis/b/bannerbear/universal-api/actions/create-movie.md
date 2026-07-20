# Bannerbear: Create Movie

Creates a new movie in Bannerbear.

```
POST https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-movie
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-movie" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "width": 1,
  "height": 1,
  "inputs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-movie', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "width": 1,
    "height": 1,
    "inputs[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `width` | number | yes | The desired width of your movie. |
| `height` | number | yes | The desired height of your movie. |
| `inputs[]` | array<object> | yes | A list of videos or images you want to combine into a movie. |
| `inputs[].asset_url` | string | no | URL to a video file or static image. |
| `inputs[].trim_to_length_in_seconds` | number | no | Force trim the end video to a specific time. |
| `inputs[].mute` | boolean | no | Remove the sound from this video clip. |
| `inputs[].soundtrack_url` | string | no | URL to an audio file to overlay on top of this clip. |
| `transition` | string | no | The name of the transition to use between video clips. |
| `soundtrack_url` | string | no | URL to an audio file to overlay on top of the movie. |
| `webhook_url` | string | no | A URL to POST the full Movie object to upon rendering completion. |
| `metadata` | string | no | Any metadata that you need to store, for example a record ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbear API returns.

## Native endpoint

Through the native Bannerbear API, this operation is `POST /v2/movies` (base URL `https://api.bannerbear.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-movie.md) for the provider-specific parameters and requirements.

