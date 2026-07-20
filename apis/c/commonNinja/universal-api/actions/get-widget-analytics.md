# Common Ninja: Get Widget Analytics

Retrieves widget analytics from Common Ninja.

```
GET https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-analytics?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-analytics?${params}`, {
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
| `breakdown` | string | no | Analytics breakdown value. |
| `endDate` | string | no | End date for the analytics period. |
| `events` | string | no | Comma-separated analytics events to include. |
| `id` | string | yes | The widget ID. |
| `startDate` | string | no | Start date for the analytics period. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dates": [
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
| `dates` | array<object> |  |

## Native endpoint

Through the native Common Ninja API, this operation is `GET /widgets/:id/analytics` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget-analytics.md) for the provider-specific parameters and requirements.

