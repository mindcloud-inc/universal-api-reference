# KEYZY: Get Encrypted License File

Validates a KEYZY license and retrieves an encrypted license file.

```
GET https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/get-encrypted-license-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/get-encrypted-license-file?connectionId=$CONNECTION_ID&code=string&serial=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string",
  "serial": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/get-encrypted-license-file?${params}`, {
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
| `code` | string | yes | A product code. |
| `deviceTag` | string | no | An operating system and bits information string. |
| `hostId` | string | no | An id to recognize the device. |
| `serial` | string | yes | A license serial number to validate. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KEYZY API returns.

## Native endpoint

Through the native KEYZY API, this operation is `POST /licenses/encrypted-file` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-encrypted-license-file.md) for the provider-specific parameters and requirements.

