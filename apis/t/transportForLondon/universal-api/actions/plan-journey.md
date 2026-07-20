# Transport for London: Plan Journey

Plans a journey between locations in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/plan-journey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/plan-journey?connectionId=$CONNECTION_ID&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/plan-journey?${params}`, {
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
| `from` | string | yes | Journey origin: coordinates, postcode, Naptan ID, Stop ID, or free text. |
| `to` | string | yes | Journey destination: coordinates, postcode, Naptan ID, Stop ID, or free text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | string | no | Optional comma-separated journey modes, such as tube,bus,walking. |
| `date` | string | no | Optional journey date in yyyyMMdd format. |
| `time` | string | no | Optional journey time in HHmm format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "journeys": [
        {}
      ],
      "lines": [
        {}
      ],
      "recommendedMaxAgeMinutes": 1,
      "searchCriteria": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `journeys` | array<object> |  |
| `lines` | array<object> |  |
| `recommendedMaxAgeMinutes` | number |  |
| `searchCriteria` | object |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Journey/JourneyResults/:from/to/:to` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/plan-journey.md) for the provider-specific parameters and requirements.

