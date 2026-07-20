# Countly: Get Large Segmentation Metadata

Retrieves large segmentation metadata from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-large-segmentation-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-large-segmentation-metadata?connectionId=$CONNECTION_ID&appId=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-large-segmentation-metadata?${params}`, {
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
| `appId` | string | yes | Countly app ID to query large segmentation metadata for. |
| `event` | string | yes | Event key to query large segmentation metadata for. |
| `prop` | string | no | Property for large segmentation metadata, such as up.src or up.lv. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no | Regex search in segment values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `values` | array<object> | Large segmentation metadata values when Countly has matching segment values. |

## Native endpoint

Through the native Countly API, this operation is `GET /o` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-large-segmentation-metadata.md) for the provider-specific parameters and requirements.

