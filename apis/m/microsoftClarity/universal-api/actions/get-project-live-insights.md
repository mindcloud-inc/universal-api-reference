# Microsoft Clarity: Get Project Live Insights

Retrieves project live insights from Microsoft Clarity.

```
GET https://connect.mindcloud.co/v1/universal/microsoftClarity/latest/actions/get-project-live-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Clarity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftClarity/latest/actions/get-project-live-insights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftClarity/latest/actions/get-project-live-insights?${params}`, {
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
| `numOfDays` | number | no | Number of days to export from the current time. Allowed values are 1, 2, or 3. Default: `1`. |
| `dimension1` | list<string> | no | The first dimension used to break down insights. Allowed values are Browser, Device, Country/Region, OS, Source, Medium, Campaign, Channel, or URL. One of: `Browser`, `Campaign`, `Channel`, `Country/Region`, `Device`, `Medium`, `OS`, `Source`, `URL`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dimension2` | list<string> | no | The second dimension used to break down insights. Allowed values are Browser, Device, Country/Region, OS, Source, Medium, Campaign, Channel, or URL. One of: `Browser`, `Campaign`, `Channel`, `Country/Region`, `Device`, `Medium`, `OS`, `Source`, `URL`. |
| `dimension3` | list<string> | no | The third dimension used to break down insights. Allowed values are Browser, Device, Country/Region, OS, Source, Medium, Campaign, Channel, or URL. One of: `Browser`, `Campaign`, `Channel`, `Country/Region`, `Device`, `Medium`, `OS`, `Source`, `URL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "information": [
        {}
      ],
      "metricName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `information` | array<object> | Metric rows returned by Microsoft Clarity for the selected lookback window. |
| `metricName` | string | Microsoft Clarity metric name for this insight block. |

## Native endpoint

Through the native Microsoft Clarity API, this operation is `GET /export-data/api/v1/project-live-insights` (base URL `https://www.clarity.ms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-live-insights.md) for the provider-specific parameters and requirements.

