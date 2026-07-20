# Bokun: List Experience Availability Statistics

Retrieves availability statistics for an experience product from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-availability-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-availability-statistics?connectionId=$CONNECTION_ID&experienceId=1&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experienceId": "1",
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-availability-statistics?${params}`, {
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
| `experienceId` | number | yes | The Bokun experience ID. |
| `from` | string | yes | The start date in yyyy-MM-dd format. |
| `to` | string | yes | The end date in yyyy-MM-dd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closed": true,
      "date": "string",
      "guidedLanguages": [
        "string"
      ],
      "id": "string",
      "initialPax": 1,
      "initialPickups": 1,
      "minPax": 1,
      "pastCutoff": true,
      "paxBooked": 1,
      "pickupsBooked": 1,
      "recurrenceRuleId": 1,
      "remainingPax": 1,
      "remainingPickups": 1,
      "remainingResources": 1,
      "startTimeId": 1,
      "time": "string",
      "tooEarly": true,
      "unlimited": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | boolean |  |
| `date` | string |  |
| `guidedLanguages` | array<string> |  |
| `id` | string |  |
| `initialPax` | number |  |
| `initialPickups` | number |  |
| `minPax` | number |  |
| `pastCutoff` | boolean |  |
| `paxBooked` | number |  |
| `pickupsBooked` | number |  |
| `recurrenceRuleId` | number |  |
| `remainingPax` | number |  |
| `remainingPickups` | number |  |
| `remainingResources` | number |  |
| `startTimeId` | number |  |
| `time` | string |  |
| `tooEarly` | boolean |  |
| `unlimited` | boolean |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/availability/:experienceId/statistics` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experience-availability-statistics.md) for the provider-specific parameters and requirements.

