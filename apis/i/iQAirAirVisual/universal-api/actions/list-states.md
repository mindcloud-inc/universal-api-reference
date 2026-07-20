# IQAir AirVisual: List States



```
GET https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IQAir AirVisual `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-states?connectionId=$CONNECTION_ID&country=USA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "USA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-states?${params}`, {
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
| `country` | string | yes | Country name exactly as returned by the List Countries action. Example: `USA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | string | State name returned for the selected country. |

## Native endpoint

Through the native IQAir AirVisual API, this operation is `GET /v2/states` (base URL `https://api.airvisual.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-states.md) for the provider-specific parameters and requirements.

