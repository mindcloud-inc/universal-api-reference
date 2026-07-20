# Countly: Get Segmentation Metadata

Retrieves all segmentation metadata from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-segmentation-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-segmentation-metadata?connectionId=$CONNECTION_ID&appId=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-segmentation-metadata?${params}`, {
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
| `appId` | string | yes | Countly app ID to query segmentation metadata for. |
| `event` | string | yes | Event key to query segmentation metadata for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "e": "string",
      "sg": {},
      "up": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `e` | string |  |
| `sg` | object |  |
| `up` | object |  |

## Native endpoint

Through the native Countly API, this operation is `GET /o` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segmentation-metadata.md) for the provider-specific parameters and requirements.

