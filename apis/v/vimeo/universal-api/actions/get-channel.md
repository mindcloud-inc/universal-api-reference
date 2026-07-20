# Vimeo: Get Channel

Retrieves a channel record from Vimeo.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-channel?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | number | yes | The ID of the channel. |
| `sizes` | string | no | The pixel dimensions of the image in {width}x{height} format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "header": {},
      "link": "https://example.com",
      "metadata": {},
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pictures": {},
      "privacy": {},
      "resourceKey": "string",
      "tags": [
        {}
      ],
      "uri": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> | The channel categories. |
| `createdTime` | date | When the channel was created. |
| `description` | string | The channel description, when present. |
| `header` | object | The channel header image object. |
| `link` | string | The public Vimeo URL for the channel. |
| `metadata` | object | The channel metadata connections and interactions. |
| `modifiedTime` | date | When the channel was last modified. |
| `name` | string | The channel name. |
| `pictures` | object | The channel pictures object. |
| `privacy` | object | The channel privacy settings. |
| `resourceKey` | string | The Vimeo resource key for the channel. |
| `tags` | array<object> | The tags associated with the channel. |
| `uri` | string | The channel URI. |
| `user` | object | The channel owner. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /channels/:channel_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

