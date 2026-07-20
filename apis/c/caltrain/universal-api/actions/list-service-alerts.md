# Caltrain: List Service Alerts

Retrieves Caltrain service alerts.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-service-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-service-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-service-alerts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Alert": {},
      "Id": "string",
      "Source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Alert` | object |  |
| `Id` | string |  |
| `Source` | string |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /gtfs/api/v1/servicealerts/Caltrain` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-alerts.md) for the provider-specific parameters and requirements.

