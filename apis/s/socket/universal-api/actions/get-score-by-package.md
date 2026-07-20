# Socket: Get Score by Package

Retrieves a package score from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-score-by-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-score-by-package?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-score-by-package?${params}`, {
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
      "depscore": 1,
      "license": {
        "components": {},
        "limit": 1,
        "limitingMetric": "string",
        "score": 1
      },
      "maintenance": {
        "components": {},
        "limit": 1,
        "limitingMetric": "string",
        "score": 1
      },
      "miscellaneous": {
        "components": {},
        "limit": 1,
        "limitingMetric": "string",
        "score": 1
      },
      "quality": {
        "components": {},
        "limit": 1,
        "limitingMetric": "string",
        "score": 1
      },
      "supplyChainRisk": {
        "components": {},
        "limit": 1,
        "limitingMetric": "string",
        "score": 1
      },
      "vulnerability": {
        "components": {},
        "limit": 1,
        "limitingMetric": "string",
        "score": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `depscore` | number |  |
| `license` | object |  |
| `license.components` | object |  |
| `license.limit` | number |  |
| `license.limitingMetric` | string |  |
| `license.score` | number |  |
| `maintenance` | object |  |
| `maintenance.components` | object |  |
| `maintenance.limit` | number |  |
| `maintenance.limitingMetric` | string |  |
| `maintenance.score` | number |  |
| `miscellaneous` | object |  |
| `miscellaneous.components` | object |  |
| `miscellaneous.limit` | number |  |
| `miscellaneous.limitingMetric` | string |  |
| `miscellaneous.score` | number |  |
| `quality` | object |  |
| `quality.components` | object |  |
| `quality.limit` | number |  |
| `quality.limitingMetric` | string |  |
| `quality.score` | number |  |
| `supplyChainRisk` | object |  |
| `supplyChainRisk.components` | object |  |
| `supplyChainRisk.limit` | number |  |
| `supplyChainRisk.limitingMetric` | string |  |
| `supplyChainRisk.score` | number |  |
| `vulnerability` | object |  |
| `vulnerability.components` | object |  |
| `vulnerability.limit` | number |  |
| `vulnerability.limitingMetric` | string |  |
| `vulnerability.score` | number |  |

## Native endpoint

Through the native Socket API, this operation is `GET /npm/:package/:version/score` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-score-by-package.md) for the provider-specific parameters and requirements.

