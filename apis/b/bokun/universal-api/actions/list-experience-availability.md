# Bokun: List Experience Availability

Retrieves availability for an experience product from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-availability?connectionId=$CONNECTION_ID&experienceId=1&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experienceId": "1",
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-availability?${params}`, {
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
      "date": "string",
      "guidedLanguages": [
        "string"
      ],
      "id": "string",
      "minPax": 1,
      "remainingPax": 1,
      "remainingPickups": 1,
      "startTimeId": 1,
      "time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `guidedLanguages` | array<string> |  |
| `id` | string |  |
| `minPax` | number |  |
| `remainingPax` | number |  |
| `remainingPickups` | number |  |
| `startTimeId` | number |  |
| `time` | string |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/availability/:experienceId` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experience-availability.md) for the provider-specific parameters and requirements.

