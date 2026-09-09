# Walmart: Discard Label

Mark a generated label as discarded.

```
DELETE https://connect.mindcloud.co/v1/universal/walmart/latest/actions/discard-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/discard-label?connectionId=$CONNECTION_ID&carrierShortName=Ava%20Chen&trackingNo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "carrierShortName": "Ava Chen",
  "trackingNo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/discard-label?${params}`, {
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
| `carrierShortName` | string | yes | `carrierShortName` from getCarriers API |
| `trackingNo` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | boolean | returns 'true' if the label is successfully discarded. |

## Native endpoint

Through the native Walmart API, this operation is `DELETE /v3/shipping/labels/carriers/:carrierShortName/trackings/:trackingNo` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/discard-label.md) for the provider-specific parameters and requirements.

