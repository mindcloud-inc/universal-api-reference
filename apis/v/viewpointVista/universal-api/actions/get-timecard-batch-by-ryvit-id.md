# Viewpoint Vista: Get Timecard Batch by Ryvit ID



```
GET https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-timecard-batch-by-ryvit-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-timecard-batch-by-ryvit-id?connectionId=$CONNECTION_ID&ryvitIdValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ryvitIdValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-timecard-batch-by-ryvit-id?${params}`, {
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
| `ryvitIdValue` | string | yes | The code of the data object you want to get. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `GET v1/direct/subscribers/{{credentials.subscriberCode}}/vista/pr/2/data/time_batches/cache/:ryvitId_value` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timecard-batch-by-ryvit-id.md) for the provider-specific parameters and requirements.

