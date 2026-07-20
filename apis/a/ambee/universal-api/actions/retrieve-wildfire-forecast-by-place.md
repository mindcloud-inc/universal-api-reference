# Ambee: Retrieve Wildfire Forecast By Place

Retrieves wildfire risk forecasts in Ambee by place name.

```
GET https://connect.mindcloud.co/v1/universal/ambee/latest/actions/retrieve-wildfire-forecast-by-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ambee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ambee/latest/actions/retrieve-wildfire-forecast-by-place?connectionId=$CONNECTION_ID&place=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "place": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ambee/latest/actions/retrieve-wildfire-forecast-by-place?${params}`, {
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
| `place` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ambee API returns.

## Native endpoint

Through the native Ambee API, this operation is `GET /fire/risk/by-place` (base URL `https://api.ambeedata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-wildfire-forecast-by-place.md) for the provider-specific parameters and requirements.

