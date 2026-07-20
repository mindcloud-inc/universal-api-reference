# Bureau of Labor Statistics Universal API Examples

These examples use the MindCloud API key and Bureau of Labor Statistics connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Latest Series Data

Retrieves the latest data point for a Bureau of Labor Statistics series.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-latest-series-data?connectionId=$CONNECTION_ID&seriesId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "seriesId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-latest-series-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "message": [
        "string"
      ],
      "responseTime": 1,
      "Results": {
        "series": [
          {
            "data": [
              {
                "footnotes": [
                  {
                    "code": "string",
                    "text": "string"
                  }
                ],
                "latest": "string",
                "period": "string",
                "periodName": "Ava Chen",
                "value": "string",
                "year": "string"
              }
            ],
            "seriesID": "string"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Latest Series Data action reference](actions/get-latest-series-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bureauOfLaborStatistics/latest/actions/get-latest-series-data).
