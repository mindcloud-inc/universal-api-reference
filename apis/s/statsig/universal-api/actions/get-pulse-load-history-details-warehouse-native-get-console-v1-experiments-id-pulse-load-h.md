# Statsig: Get Pulse Load History Details (Warehouse Native)

Retrieves warehouse-native pulse load history details from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-pulse-load-history-details-warehouse-native-get-console-v1-experiments-id-pulse-load-h
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-pulse-load-history-details-warehouse-native-get-console-v1-experiments-id-pulse-load-h?connectionId=$CONNECTION_ID&id=string&dagID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "dagID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-pulse-load-history-details-warehouse-native-get-console-v1-experiments-id-pulse-load-h?${params}`, {
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
| `id` | string | yes | id |
| `dagID` | string | yes | dagID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/experiments/{id}/pulse_load_history/{dagID}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pulse-load-history-details-warehouse-native-get-console-v1-experiments-id-pulse-load-h.md) for the provider-specific parameters and requirements.

