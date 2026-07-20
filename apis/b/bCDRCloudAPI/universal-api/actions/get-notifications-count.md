# BCDR Cloud: Get Notifications Count



```
GET https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-notifications-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BCDR Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-notifications-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-notifications-count?${params}`, {
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
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Current notification count returned by the endpoint. |

## Native endpoint

Through the native BCDR Cloud API, this operation is `POST /getnotificationscount` (base URL `https://console1.bdrshield.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notifications-count.md) for the provider-specific parameters and requirements.

