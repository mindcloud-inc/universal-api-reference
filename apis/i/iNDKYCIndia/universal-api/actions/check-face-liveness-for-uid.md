# IN-D KYC India: Check Face Liveness For UID

Retrieves face liveness results in IN-D KYC India by UID.

```
GET https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/check-face-liveness-for-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IN-D KYC India `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/check-face-liveness-for-uid?connectionId=$CONNECTION_ID&uid=test-uid&image=iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8%2Fx8AAwMCAO%2B%2Fp9sAAAAASUVORK5CYII%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "test-uid",
  "image": "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8/x8AAwMCAO+/p9sAAAAASUVORK5CYII="
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/check-face-liveness-for-uid?${params}`, {
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
| `uid` | string | yes | UID returned by Generate UID. Default: `test-uid`. |
| `image` | string | yes | Base64-encoded face image content. Default: `iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8/x8AAwMCAO+/p9sAAAAASUVORK5CYII=`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | object | Face liveness status wrapper from IN-D. |

## Native endpoint

Through the native IN-D KYC India API, this operation is `POST /api/facelivenessv2/{uid}` (base URL `https://api.kyc.in-d.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-face-liveness-for-uid.md) for the provider-specific parameters and requirements.

