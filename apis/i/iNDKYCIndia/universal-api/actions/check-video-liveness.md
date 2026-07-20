# IN-D KYC India: Check Video Liveness

Retrieves video liveness results from IN-D KYC India.

```
GET https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/check-video-liveness
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IN-D KYC India `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/check-video-liveness?connectionId=$CONNECTION_ID&term=hello&video=YmFzZTY0IHZpZGVv&language=en" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "hello",
  "video": "YmFzZTY0IHZpZGVv",
  "language": "en"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/check-video-liveness?${params}`, {
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
| `term` | string | yes | Term or phrase expected in the video liveness check. Default: `hello`. |
| `video` | string | yes | Base64-encoded video content. Default: `YmFzZTY0IHZpZGVv`. |
| `language` | string | yes | Language code for the liveness term. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | object | Video liveness result message. |

## Native endpoint

Through the native IN-D KYC India API, this operation is `POST /api/liveliness/` (base URL `https://api.kyc.in-d.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-video-liveness.md) for the provider-specific parameters and requirements.

