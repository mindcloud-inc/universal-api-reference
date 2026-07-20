# Timekit: Get Availability Dates

Retrieves available booking dates from Timekit.

```
GET https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-availability-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-availability-dates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-availability-dates?${params}`, {
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
| `from` | string | no | Beginning of the search space. |
| `projectId` | string | no | Project ID to derive availability settings from. |
| `resources[]` | array<string> | no | Resource IDs to include in the availability search. |
| `to` | string | no | End of the search space. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "resources": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `resources` | array<string> |  |

## Native endpoint

Through the native Timekit API, this operation is `POST /availability/dates` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-availability-dates.md) for the provider-specific parameters and requirements.

