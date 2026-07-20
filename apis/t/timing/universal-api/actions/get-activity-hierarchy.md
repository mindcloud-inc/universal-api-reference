# Timing: Get Activity Hierarchy

Retrieves the activity hierarchy from Timing.

```
GET https://connect.mindcloud.co/v1/universal/timing/latest/actions/get-activity-hierarchy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timing/latest/actions/get-activity-hierarchy?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timing/latest/actions/get-activity-hierarchy?${params}`, {
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
| `startDate` | string | yes | Start of the activity range. Timing accepts a date or timestamp. |
| `endDate` | string | yes | End of the activity range. Timing accepts a date or timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Timing API, this operation is `GET /activity-hierarchy` (base URL `https://web.timingapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity-hierarchy.md) for the provider-specific parameters and requirements.

