# Grafana: Get Annotation By ID

Retrieves an annotation from Grafana by ID.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-annotation-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-annotation-by-id?connectionId=$CONNECTION_ID&annotationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "annotationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-annotation-by-id?${params}`, {
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
| `annotationId` | number | yes | The annotation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertId": 1,
      "dashboardId": 1,
      "id": 1,
      "text": "string",
      "time": 1,
      "timeEnd": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertId` | number |  |
| `dashboardId` | number |  |
| `id` | number |  |
| `text` | string |  |
| `time` | number |  |
| `timeEnd` | number |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /annotations/:annotation_id` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-annotation-by-id.md) for the provider-specific parameters and requirements.

