# Grafana: Get Data Source By Name

Retrieves a data source from Grafana by name.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-data-source-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-data-source-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-data-source-by-name?${params}`, {
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
| `name` | string | yes | The data source name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen",
      "readOnly": true,
      "type": "string",
      "uid": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `readOnly` | boolean |  |
| `type` | string |  |
| `uid` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /datasources/name/:name` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-source-by-name.md) for the provider-specific parameters and requirements.

