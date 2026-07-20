# Tophhie Cloud: Get Apple OS Version

Retrieves the latest Apple OS version for a device in Tophhie Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-apple-os-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-apple-os-version?connectionId=$CONNECTION_ID&appleDeviceModel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appleDeviceModel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-apple-os-version?${params}`, {
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
| `appleDeviceModel` | string | yes | Apple hardware identifier, for example iPhone17,1. |
| `currentOSVersion` | string | no | Current Apple OS version to compare against. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appleDeviceModel": "string",
      "errorMessage": "string",
      "latestVersion": "string",
      "os": "string",
      "support": {},
      "updatePosted": "2026-05-07T12:00:00.000Z",
      "updateRequired": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appleDeviceModel` | string | Apple hardware identifier. |
| `errorMessage` | string | Error message when present. |
| `latestVersion` | string | Latest available OS version. |
| `os` | string | Apple operating system family. |
| `support` | object | Tophhie Cloud API support details. |
| `updatePosted` | date | Date the latest update was posted. |
| `updateRequired` | boolean | Whether the current version needs an update. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /appleosversion/{appleDeviceModel}` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-apple-os-version.md) for the provider-specific parameters and requirements.

