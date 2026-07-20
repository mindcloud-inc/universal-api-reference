# Timekit: Get Availability Counts

Retrieves available timeslot counts from Timekit.

```
GET https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-availability-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-availability-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-availability-counts?${params}`, {
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
| `buffer` | string | no |  |
| `from` | string | no |  |
| `length` | string | no |  |
| `projectId` | string | no |  |
| `resources[]` | array<string> | no |  |
| `timeslotIncrements` | string | no |  |
| `to` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |

## Native endpoint

Through the native Timekit API, this operation is `POST /availability/count` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-availability-counts.md) for the provider-specific parameters and requirements.

