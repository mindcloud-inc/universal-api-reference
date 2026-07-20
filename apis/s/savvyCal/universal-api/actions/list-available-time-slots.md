# SavvyCal: List Available Time Slots



```
GET https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-available-time-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SavvyCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-available-time-slots?connectionId=$CONNECTION_ID&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-available-time-slots?${params}`, {
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
| `linkId` | string | yes |  |
| `from` | date | no |  |
| `until` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "endAt": "2026-05-07T12:00:00.000Z",
      "rank": 1,
      "startAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number | Slot duration in minutes. |
| `endAt` | date | Slot end time. |
| `rank` | number | Slot ranking or priority. |
| `startAt` | date | Slot start time. |

## Native endpoint

Through the native SavvyCal API, this operation is `GET /v1/links/:link_id/slots` (base URL `https://api.savvycal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-time-slots.md) for the provider-specific parameters and requirements.

