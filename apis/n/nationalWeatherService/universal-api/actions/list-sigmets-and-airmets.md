# National Weather Service: List SIGMETs And AIRMETs

Retrieves SIGMETs and AIRMETs from National Weather Service.

```
GET https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/list-sigmets-and-airmets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Weather Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/list-sigmets-and-airmets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/list-sigmets-and-airmets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native National Weather Service API returns.

## Native endpoint

Through the native National Weather Service API, this operation is `GET /aviation/sigmets` (base URL `https://api.weather.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sigmets-and-airmets.md) for the provider-specific parameters and requirements.

