# Shotstack: Inspect Media



```
GET https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/inspect-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/inspect-media?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/inspect-media?${params}`, {
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
| `url` | string | yes | The public URL of the media file to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Probe metadata for the inspected media URL. |

## Native endpoint

Through the native Shotstack API, this operation is `GET /edit/v1/probe/:url` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inspect-media.md) for the provider-specific parameters and requirements.

