# ImageKit.io: Get Usage

Retrieves account usage metrics from ImageKit.io.

```
GET https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-usage?${params}`, {
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
| `endDate` | string | no |  |
| `startDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bandwidthBytes": 1,
      "extensionUnitsCount": 1,
      "mediaLibraryStorageBytes": 1,
      "originalCacheStorageBytes": 1,
      "videoProcessingUnitsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bandwidthBytes` | number |  |
| `extensionUnitsCount` | number |  |
| `mediaLibraryStorageBytes` | number |  |
| `originalCacheStorageBytes` | number |  |
| `videoProcessingUnitsCount` | number |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `GET /accounts/usage` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

