# Socket: Get Trend of Historical Dependencies

Retrieves historical dependency trends from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-trend-of-historical-dependencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-trend-of-historical-dependencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-trend-of-historical-dependencies?${params}`, {
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
      "items": [
        {
          "dataPoints": [
            {}
          ],
          "date": "string",
          "startOfDayTimestamp": 1
        }
      ],
      "meta": {
        "aggregation": {
          "fields": [
            "string"
          ],
          "groups": [
            [
              "string"
            ]
          ]
        },
        "endDateInclusive": "string",
        "filters": {
          "artifactType": [
            "string"
          ],
          "dependencyDead": [
            true
          ],
          "dependencyDev": [
            true
          ],
          "dependencyDirect": [
            true
          ],
          "repoFullName": [
            "Ava Chen"
          ],
          "repoLabels": [
            "string"
          ],
          "repoSlug": [
            "string"
          ]
        },
        "interval": "string",
        "organizationId": "string",
        "startDateInclusive": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[]` | object |  |
| `items[].dataPoints` | array<object> |  |
| `items[].dataPoints[]` | object |  |
| `items[].date` | string |  |
| `items[].startOfDayTimestamp` | number |  |
| `meta` | object |  |
| `meta.aggregation` | object |  |
| `meta.aggregation.fields` | array<string> |  |
| `meta.aggregation.groups` | array<array> |  |
| `meta.aggregation.groups[]` | array |  |
| `meta.endDateInclusive` | string |  |
| `meta.filters` | object |  |
| `meta.filters.artifactType` | array<string> |  |
| `meta.filters.dependencyDead` | array<boolean> |  |
| `meta.filters.dependencyDev` | array<boolean> |  |
| `meta.filters.dependencyDirect` | array<boolean> |  |
| `meta.filters.repoFullName` | array<string> |  |
| `meta.filters.repoLabels` | array<string> |  |
| `meta.filters.repoSlug` | array<string> |  |
| `meta.interval` | string |  |
| `meta.organizationId` | string |  |
| `meta.startDateInclusive` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/historical/dependencies/trend` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trend-of-historical-dependencies.md) for the provider-specific parameters and requirements.

