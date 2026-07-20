# Countly: Get Segmentation

Retrieves all segmentation data from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-segmentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-segmentation?connectionId=$CONNECTION_ID&appId=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-segmentation?${params}`, {
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
| `appId` | string | yes | Countly app ID to query segmentation for. |
| `period` | string | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
| `event` | string | yes | Event key to query segmentation for. |
| `bucket` | string | no | Breakdown period for segmentation, such as hourly, daily, weekly, or monthly. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectionKey` | string | no | Show top results by a specific segment value. |
| `queryObject` | string | no | JSON string encoded MongoDB query for segmentation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Segmentation analytics response for the requested event and bucket. |

## Native endpoint

Through the native Countly API, this operation is `GET /o` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segmentation.md) for the provider-specific parameters and requirements.

