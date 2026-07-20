# Notify: Get Current Channel QR Code

Retrieves the current channel QR code from Notify.

```
GET https://connect.mindcloud.co/v1/universal/notify/latest/actions/get-current-channel-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notify/latest/actions/get-current-channel-qr-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notify/latest/actions/get-current-channel-qr-code?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | The QR code SVG bytes. |
| `type` | string | The runtime wrapper type for the raw SVG response. |

## Native endpoint

Through the native Notify API, this operation is `GET /{{credentials.channelToken}}/qr.svg` (base URL `https://notify.run`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-channel-qr-code.md) for the provider-specific parameters and requirements.

