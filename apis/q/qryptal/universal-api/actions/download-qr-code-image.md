# Qryptal: Download QR Code Image



```
GET https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/download-qr-code-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qryptal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/download-qr-code-image?connectionId=$CONNECTION_ID&uid=1097580178100010000601672116&codeToken=C02%3ArFKsq1dyUmJZZFNze1Jr..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "1097580178100010000601672116",
  "codeToken": "C02:rFKsq1dyUmJZZFNze1Jr..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/download-qr-code-image?${params}`, {
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
| `uid` | string | yes | Unique Qryptal identifier returned when the QR code was created. Example: `1097580178100010000601672116`. |
| `codeToken` | string | yes | The code_token value returned by QR creation. Example: `C02:rFKsq1dyUmJZZFNze1Jr...`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bg` | number | no | Set to 0 to request a transparent background. Example: `0`. |
| `size` | number | no | Optional image size selector documented by Qryptal. Example: `4`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Qryptal API returns.

## Native endpoint

Through the native Qryptal API, this operation is `GET :uid/qr:uid.png` (base URL `https://api2test.qryptal.com/v2/Vqodes/v2/Vqodes/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-qr-code-image.md) for the provider-specific parameters and requirements.

