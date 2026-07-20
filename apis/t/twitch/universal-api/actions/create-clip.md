# Twitch: Create Clip

Creates a new clip in Twitch.

```
POST https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-clip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-clip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-clip', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | The broadcaster whose live stream to clip. |
| `title` | string | no | Optional title for the clip. |
| `duration` | number | no | Clip length in seconds. Possible values range from 5 to 60 with 0.1 precision. Default is 30. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "editUrl": "https://example.com",
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | A list containing the created clip. |
| `data[].editUrl` | string | URL used to edit and publish the clip. |
| `data[].id` | string | Clip identifier. |

## Native endpoint

Through the native Twitch API, this operation is `POST /clips` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-clip.md) for the provider-specific parameters and requirements.

