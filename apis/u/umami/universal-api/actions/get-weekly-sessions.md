# Umami: Get Weekly Sessions



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-weekly-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-weekly-sessions?connectionId=$CONNECTION_ID&websiteId=string&startAt=1&endAt=1&timezone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1",
  "timezone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-weekly-sessions?${params}`, {
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
| `websiteId` | string | yes | The website ID. |
| `startAt` | number | yes | Start timestamp in milliseconds. |
| `endAt` | number | yes | End timestamp in milliseconds. |
| `timezone` | string | yes | Timezone like America/Los_Angeles. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | array<array> | Seven-day by twenty-four-hour weekly sessions heatmap matrix. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/sessions/weekly` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-weekly-sessions.md) for the provider-specific parameters and requirements.

