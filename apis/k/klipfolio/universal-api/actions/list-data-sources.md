# Klipfolio: List Data Sources

Retrieves a list of data sources from Klipfolio.

```
GET https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klipfolio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-data-sources?${params}`, {
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
      "date_last_refresh": "string",
      "description": "string",
      "id": "string",
      "is_dynamic": true,
      "name": "Ava Chen",
      "refresh_interval": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_last_refresh` | string |  |
| `description` | string |  |
| `id` | string |  |
| `is_dynamic` | boolean |  |
| `name` | string |  |
| `refresh_interval` | number |  |

## Native endpoint

Through the native Klipfolio API, this operation is `GET /datasources` (base URL `https://app.klipfolio.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-sources.md) for the provider-specific parameters and requirements.

