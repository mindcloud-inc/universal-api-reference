# 2Smart Cloud: Pie statistics



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-statistics-version-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-statistics-version-progress?connectionId=$CONNECTION_ID&product_id=1&version=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "product_id": "1",
  "version": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-statistics-version-progress?${params}`, {
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
| `product_id` | number | yes | ID of product |
| `version` | number | yes | Version of firmware |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all_devices_ready": 1,
      "current_version_devices_ready": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all_devices_ready` | number |  |
| `current_version_devices_ready` | number |  |
| `version` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/statistics/version-progress` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-statistics-version-progress.md) for the provider-specific parameters and requirements.

