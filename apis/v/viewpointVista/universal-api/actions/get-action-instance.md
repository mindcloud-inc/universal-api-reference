# Viewpoint Vista: Get Action Instance

Vista processes write operations asynchronously. This endpoint allows the integration to confirm whether a batch or time entry was successfully created.

```
GET https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-action-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-action-instance?connectionId=$CONNECTION_ID&action_key_value=action-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "action_key_value": "action-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-action-instance?${params}`, {
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
| `action_key_value` | string | yes | Action Instance Identifier returned by an asynchronous Vista write operation. Example: `action-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionCode": "string",
      "createdUtc": "string",
      "dataObjectCode": "string",
      "id": "string",
      "result": {
        "batchId": 1
      },
      "status": "string",
      "subscriberCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionCode` | string |  |
| `createdUtc` | string |  |
| `dataObjectCode` | string |  |
| `id` | string |  |
| `result` | object |  |
| `result.batchId` | number | Numeric Vista timecard batch ID returned when the asynchronous batch action succeeds. |
| `status` | string |  |
| `subscriberCode` | string |  |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `GET v1/direct/actions/:action_key_value` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action-instance.md) for the provider-specific parameters and requirements.

