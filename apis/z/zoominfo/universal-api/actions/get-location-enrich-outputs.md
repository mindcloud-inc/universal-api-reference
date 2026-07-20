# Zoominfo: Get Location Enrich Outputs

Retrieves location enrich output fields from ZoomInfo.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-location-enrich-outputs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-location-enrich-outputs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-location-enrich-outputs?${params}`, {
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
      "accessGranted": "string",
      "description": "string",
      "fieldName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessGranted` | string |  |
| `description` | string |  |
| `fieldName` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `GET lookup/outputfields/location/enrich` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-enrich-outputs.md) for the provider-specific parameters and requirements.

