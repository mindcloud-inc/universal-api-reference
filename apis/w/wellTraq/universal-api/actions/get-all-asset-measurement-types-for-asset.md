# WellTraq: Get All Asset Measurement Types For Asset

Retrieves asset measurement types for an asset from WellTraq.

```
GET https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-all-asset-measurement-types-for-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WellTraq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-all-asset-measurement-types-for-asset?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-all-asset-measurement-types-for-asset?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `unit` | string |  |

## Native endpoint

Through the native WellTraq API, this operation is `GET /AssetMeasurementTypes/GetAllForAsset` (base URL `https://welltraq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-asset-measurement-types-for-asset.md) for the provider-specific parameters and requirements.

