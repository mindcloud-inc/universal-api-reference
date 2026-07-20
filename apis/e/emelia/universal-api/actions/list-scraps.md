# Emelia: List Scraps

Retrieves scrap listings from Emelia.

```
GET https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-scraps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-scraps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-scraps?${params}`, {
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
      "data": {
        "scraps": [
          {
            "auth": {},
            "authes": [
              "string"
            ],
            "date": "string",
            "enrichEnabled": true,
            "enrichFound": 1,
            "enrichIndex": 1,
            "error": {},
            "estimatedEnd": {},
            "name": "Ava Chen",
            "nextRunningSegment": {},
            "plannedStart": {},
            "processing": {},
            "scrapIndex": 1,
            "segmented": true,
            "status": "string",
            "totalContact": 1,
            "url": "https://example.com"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.scraps[].auth` | object |  |
| `data.scraps[].authes[]` | string |  |
| `data.scraps[].date` | string |  |
| `data.scraps[].enrichEnabled` | boolean |  |
| `data.scraps[].enrichFound` | number |  |
| `data.scraps[].enrichIndex` | number |  |
| `data.scraps[].error` | object |  |
| `data.scraps[].estimatedEnd` | object |  |
| `data.scraps[].name` | string |  |
| `data.scraps[].nextRunningSegment` | object |  |
| `data.scraps[].plannedStart` | object |  |
| `data.scraps[].processing` | object |  |
| `data.scraps[].scrapIndex` | number |  |
| `data.scraps[].segmented` | boolean |  |
| `data.scraps[].status` | string |  |
| `data.scraps[].totalContact` | number |  |
| `data.scraps[].url` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scraps.md) for the provider-specific parameters and requirements.

