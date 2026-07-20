# ShipWise: List Channel Settings V2

Retrieves channel settings from ShipWise.

```
GET https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-channel-settings-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipWise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-channel-settings-v2?connectionId=$CONNECTION_ID&linkIds=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkIds": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-channel-settings-v2?${params}`, {
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
| `linkIds` | string | yes | One or more ShipWise channel link IDs to retrieve settings for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipWise API returns.

## Native endpoint

Through the native ShipWise API, this operation is `GET /api/v2/Channel/settings` (base URL `https://api.shipwise.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-settings-v2.md) for the provider-specific parameters and requirements.

