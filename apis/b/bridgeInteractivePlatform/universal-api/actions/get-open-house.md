# Bridge Interactive Platform: Get open house

Retrieves an open house from Bridge Interactive Platform.

```
GET https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-open-house
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge Interactive Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-open-house?connectionId=$CONNECTION_ID&dataset=test&openhouseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test",
  "openhouseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-open-house?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code. This tenant was validated against dataset test. Default: `test`. |
| `openhouseId` | string | yes | Bridge open house identifier from the REST open houses feed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ListingKey": "string",
      "OpenHouseDate": "2026-05-07T12:00:00.000Z",
      "OpenHouseEndTime": "2026-05-07T12:00:00.000Z",
      "OpenHouseKey": "string",
      "OpenHouseStartTime": "2026-05-07T12:00:00.000Z",
      "ShowingAgentKey": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ListingKey` | string |  |
| `OpenHouseDate` | date |  |
| `OpenHouseEndTime` | date |  |
| `OpenHouseKey` | string |  |
| `OpenHouseStartTime` | date |  |
| `ShowingAgentKey` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Bridge Interactive Platform API, this operation is `GET /:dataset/openhouses/:openhouseId` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-open-house.md) for the provider-specific parameters and requirements.

