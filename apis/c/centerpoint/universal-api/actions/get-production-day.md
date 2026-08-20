# Centerpoint: Get Production Day



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-production-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-production-day?connectionId=$CONNECTION_ID&PRODUCTION_DAYS_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PRODUCTION_DAYS_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-production-day?${params}`, {
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
| `PRODUCTION_DAYS_ID` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[productions]` | string | no |  |
| `fields[divisions]` | string | no |  |
| `fields[assignedProductionTaskCategories]` | string | no |  |
| `fields[productionDays]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "approved": "string",
        "approvedAt": {},
        "createdAt": "string",
        "custom": {
          "arethereanyimidiateneeds": {},
          "attendance": {},
          "delay": {},
          "forecastedweather": {},
          "safetymeetingtopic": {},
          "weather": {}
        },
        "customWithLabels": {
          "areThereAnyImmediateNeeds": {},
          "attendance": {},
          "delay": {},
          "forecastedWeather": {},
          "safetyMeetingTopic": {},
          "weather": {}
        },
        "deletedAt": {},
        "isVisible": 1,
        "measurement": 1,
        "options": {
          "notes": "string",
          "sendNow": true
        },
        "photoSummary": "string",
        "productionId": 1,
        "sentAt": {},
        "sentStatus": "string",
        "updatedAt": "string",
        "uuid": "string",
        "workDate": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.approved` | string |  |
| `attributes.approvedAt` | object |  |
| `attributes.createdAt` | string |  |
| `attributes.custom.arethereanyimidiateneeds` | object |  |
| `attributes.custom.attendance` | object |  |
| `attributes.custom.delay` | object |  |
| `attributes.custom.forecastedweather` | object |  |
| `attributes.custom.safetymeetingtopic` | object |  |
| `attributes.custom.weather` | object |  |
| `attributes.customWithLabels.areThereAnyImmediateNeeds` | object |  |
| `attributes.customWithLabels.attendance` | object |  |
| `attributes.customWithLabels.delay` | object |  |
| `attributes.customWithLabels.forecastedWeather` | object |  |
| `attributes.customWithLabels.safetyMeetingTopic` | object |  |
| `attributes.customWithLabels.weather` | object |  |
| `attributes.deletedAt` | object |  |
| `attributes.isVisible` | number |  |
| `attributes.measurement` | number |  |
| `attributes.options.notes` | string |  |
| `attributes.options.sendNow` | boolean |  |
| `attributes.photoSummary` | string |  |
| `attributes.productionId` | number |  |
| `attributes.sentAt` | object |  |
| `attributes.sentStatus` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.uuid` | string |  |
| `attributes.workDate` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET production_days/:PRODUCTION_DAYS_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-production-day.md) for the provider-specific parameters and requirements.

