# Scanova: Validate QR Code Info Data



```
GET https://connect.mindcloud.co/v1/universal/scanova/latest/actions/validate-qr-code-info-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/validate-qr-code-info-data?connectionId=$CONNECTION_ID&category=string&info=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string",
  "info": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/validate-qr-code-info-data?${params}`, {
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
| `category` | string | yes | QR code category ID |
| `info` | string | yes | QR code info JSON data |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scanova API returns.

## Native endpoint

Through the native Scanova API, this operation is `POST /qr/validate-info/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-qr-code-info-data.md) for the provider-specific parameters and requirements.

