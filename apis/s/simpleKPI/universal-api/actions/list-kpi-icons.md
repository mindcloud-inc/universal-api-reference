# SimpleKPI: List KPI Icons

Retrieves KPI icon records from SimpleKPI.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpi-icons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpi-icons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpi-icons?${params}`, {
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
      "id": 1,
      "large_pos": "string",
      "name": "Ava Chen",
      "small_pos": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `large_pos` | string |  |
| `name` | string |  |
| `small_pos` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET kpiicons` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-kpi-icons.md) for the provider-specific parameters and requirements.

