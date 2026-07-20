# Calibre: List Site Metrics

Retrieves timeseries metrics for a site from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-site-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-site-metrics?connectionId=$CONNECTION_ID&variables.site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-site-metrics?${params}`, {
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
| `variables.site` | string | yes | Site slug, found in site settings. |
| `variables.measurement` | string | no | Metric tag to retrieve for the site. Default: `largestContentfulPaint`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "site": {
          "latestMetrics": {
            "data": [
              {
                "change": 1,
                "current": 1,
                "currentGrading": "string",
                "difference": 1,
                "measurement": "string",
                "page": "string",
                "previous": 1,
                "profile": "string"
              }
            ]
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organisation.site.latestMetrics.data[].change` | number |  |
| `organisation.site.latestMetrics.data[].current` | number |  |
| `organisation.site.latestMetrics.data[].currentGrading` | string |  |
| `organisation.site.latestMetrics.data[].difference` | number |  |
| `organisation.site.latestMetrics.data[].measurement` | string |  |
| `organisation.site.latestMetrics.data[].page` | string |  |
| `organisation.site.latestMetrics.data[].previous` | number |  |
| `organisation.site.latestMetrics.data[].profile` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-site-metrics.md) for the provider-specific parameters and requirements.

