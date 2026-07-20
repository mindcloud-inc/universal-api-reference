# KEYZY: Validate License

Validates a software license in KEYZY.

```
GET https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/validate-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/validate-license?connectionId=$CONNECTION_ID&code=string&serial=string&version=2.0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string",
  "serial": "string",
  "version": "2.0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/validate-license?${params}`, {
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
| `version` | string | yes | Constant value required by KEYZY. Use 2.0. Default: `2.0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "licenseeEmail": "ava@example.com",
        "licenseeName": "Ava Chen",
        "message": "string",
        "productCode": "string",
        "skuNumber": "string",
        "versionCode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.licenseeEmail` | string | Licensee email. |
| `data.licenseeName` | string | Licensee name. |
| `data.message` | string | Validation status message. |
| `data.productCode` | string | Validated product code. |
| `data.skuNumber` | string | Validated SKU number. |
| `data.versionCode` | string | Validated version code. |

## Native endpoint

Through the native KEYZY API, this operation is `POST /licenses/valid` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-license.md) for the provider-specific parameters and requirements.

