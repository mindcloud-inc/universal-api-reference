# Airzone Cloud: Get Webserver Status

Retrieves webserver status and config from Airzone Cloud.

```
GET https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-webserver-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-webserver-status?connectionId=$CONNECTION_ID&installationId=string&wsId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "installationId": "string",
  "wsId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-webserver-status?${params}`, {
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
| `devices` | string | no | Optional flag. Set to `1` to include device data when the authenticated user is an installation admin. |
| `installationId` | string | yes | The installation ID that owns the webserver. |
| `wsId` | string | yes | The Airzone webserver identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "devices": [
        {}
      ],
      "status": {},
      "ws_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object | Webserver configuration object. |
| `devices` | array<object> | Webserver devices when requested and authorized. |
| `status` | object | Webserver status object. |
| `ws_type` | string | Webserver type. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `GET /devices/ws/{wsId}/status` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webserver-status.md) for the provider-specific parameters and requirements.

