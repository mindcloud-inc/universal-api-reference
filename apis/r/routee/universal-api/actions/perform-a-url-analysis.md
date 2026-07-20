# Routee: Perform a URL analysis

Analyzes a URL request in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-url-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-url-analysis" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-url-analysis', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cache` | boolean | no | Get a cached response from our databases or get a synchronous response. |
| `domain` | string | yes | The domain for which we need an analysis. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {
        "advertisingNetwork": [
          [
            {}
          ]
        ],
        "captchas": [
          [
            {}
          ]
        ],
        "emailProviders": [
          [
            {}
          ]
        ],
        "hostingControlPanel": [
          [
            {}
          ]
        ],
        "jsLibraries": [
          [
            {}
          ]
        ],
        "miscellaneous": [
          [
            {}
          ]
        ],
        "pushNotificationProviders": [
          [
            {}
          ]
        ],
        "socialNetworks": [
          [
            {}
          ]
        ],
        "tagManager": [
          [
            {}
          ]
        ],
        "webFramework": [
          [
            {}
          ]
        ],
        "webServer": [
          [
            {}
          ]
        ],
        "widget": [
          [
            {}
          ]
        ]
      },
      "cache": true,
      "domain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis` | object |  |
| `analysis.advertisingNetwork[]` | array<object> |  |
| `analysis.advertisingNetwork[].description` | string |  |
| `analysis.advertisingNetwork[].name` | string |  |
| `analysis.captchas[]` | array<object> |  |
| `analysis.captchas[].description` | string |  |
| `analysis.captchas[].name` | string |  |
| `analysis.emailProviders[]` | array<object> |  |
| `analysis.emailProviders[].description` | string |  |
| `analysis.emailProviders[].name` | string |  |
| `analysis.hostingControlPanel[]` | array<object> |  |
| `analysis.hostingControlPanel[].description` | string |  |
| `analysis.hostingControlPanel[].name` | string |  |
| `analysis.jsLibraries[]` | array<object> |  |
| `analysis.jsLibraries[].description` | string |  |
| `analysis.jsLibraries[].name` | string |  |
| `analysis.miscellaneous[]` | array<object> |  |
| `analysis.miscellaneous[].description` | string |  |
| `analysis.miscellaneous[].name` | string |  |
| `analysis.pushNotificationProviders[]` | array<object> |  |
| `analysis.pushNotificationProviders[].description` | string |  |
| `analysis.pushNotificationProviders[].name` | string |  |
| `analysis.socialNetworks[]` | array<object> |  |
| `analysis.socialNetworks[].description` | string |  |
| `analysis.socialNetworks[].name` | string |  |
| `analysis.tagManager[]` | array<object> |  |
| `analysis.tagManager[].description` | string |  |
| `analysis.tagManager[].name` | string |  |
| `analysis.webFramework[]` | array<object> |  |
| `analysis.webFramework[].description` | string |  |
| `analysis.webFramework[].name` | string |  |
| `analysis.webServer[]` | array<object> |  |
| `analysis.webServer[].description` | string |  |
| `analysis.webServer[].name` | string |  |
| `analysis.widget[]` | array<object> |  |
| `analysis.widget[].description` | string |  |
| `analysis.widget[].name` | string |  |
| `cache` | boolean |  |
| `domain` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /urlinsights` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-a-url-analysis.md) for the provider-specific parameters and requirements.

