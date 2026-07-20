# GrowthBook: Get all rampScheduleTemplates

Retrieves rampscheduletemplates from your GrowthBook organization.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-ramp-schedule-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-ramp-schedule-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-ramp-schedule-templates?${params}`, {
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
      "rampScheduleTemplates": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rampScheduleTemplates` | array<object> |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /ramp-schedule-templates` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ramp-schedule-templates.md) for the provider-specific parameters and requirements.

