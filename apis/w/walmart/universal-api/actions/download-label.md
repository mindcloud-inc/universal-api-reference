# Walmart: Download Label

Retrieve the label for a carrier & tracking number combination. Returns PDF or PNG formatted label.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/download-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/download-label?connectionId=$CONNECTION_ID&carrierShortName=Ava%20Chen&trackingNo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "carrierShortName": "Ava Chen",
  "trackingNo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/download-label?${params}`, {
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
| `carrierShortName` | string | yes | carrierShortName |
| `trackingNo` | string | yes | The tracking number of the label to download. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list<string> | no | Defaults to PDF if not set. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Walmart API returns.

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/shipping/labels/carriers/:carrierShortName/trackings/:trackingNo` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-label.md) for the provider-specific parameters and requirements.

