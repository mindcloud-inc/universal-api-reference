# eWeLink: Get Device OTA Update Information

Retrieves device OTA update information from eWeLink.

```
GET https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-device-ota-update-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-device-ota-update-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-device-ota-update-information?${params}`, {
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
      "otaInfoList": [
        {
          "binList": [
            {
              "digest": "string",
              "downloadUrl": "https://example.com",
              "name": "Ava Chen"
            }
          ],
          "deviceid": "string",
          "forceTime": "string",
          "type": "string",
          "version": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `otaInfoList[].binList[].digest` | string |  |
| `otaInfoList[].binList[].downloadUrl` | string |  |
| `otaInfoList[].binList[].name` | string |  |
| `otaInfoList[].deviceid` | string |  |
| `otaInfoList[].forceTime` | string |  |
| `otaInfoList[].type` | string |  |
| `otaInfoList[].version` | string |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/device/ota/query` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-ota-update-information.md) for the provider-specific parameters and requirements.

