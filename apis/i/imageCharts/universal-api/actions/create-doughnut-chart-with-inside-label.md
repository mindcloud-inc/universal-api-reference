# Image-Charts: Create Doughnut Chart With Inside Label

Creates a doughnut chart with an inside label using Image-Charts.

```
GET https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-doughnut-chart-with-inside-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Image-Charts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-doughnut-chart-with-inside-label?connectionId=$CONNECTION_ID&size=string&data=string&labels=string&legend=string&insideLabel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "size": "string",
  "data": "string",
  "labels": "string",
  "legend": "string",
  "insideLabel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-doughnut-chart-with-inside-label?${params}`, {
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
| `size` | string | yes | Chart size in pixels, for example 300x200. |
| `data` | string | yes | Chart data in Image-Charts format. |
| `labels` | string | yes | Slice labels separated by pipes. |
| `legend` | string | yes | Legend entries separated by pipes. |
| `insideLabel` | string | yes | Label shown inside the doughnut chart. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native Image-Charts API, this operation is `GET /chart` (base URL `https://image-charts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-doughnut-chart-with-inside-label.md) for the provider-specific parameters and requirements.

