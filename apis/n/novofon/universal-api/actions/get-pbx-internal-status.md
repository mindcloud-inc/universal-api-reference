# Novofon: Get PBX Internal Status

Retrieves PBX internal status from Novofon.

```
GET https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-pbx-internal-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-pbx-internal-status?connectionId=$CONNECTION_ID&pbxSip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pbxSip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-pbx-internal-status?${params}`, {
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
| `pbxSip` | string | yes | PBX internal number to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isOnline": "string",
      "number": "string",
      "pbxId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isOnline` | string |  |
| `number` | string |  |
| `pbxId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/pbx/internal/:pbxSip/status/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pbx-internal-status.md) for the provider-specific parameters and requirements.

