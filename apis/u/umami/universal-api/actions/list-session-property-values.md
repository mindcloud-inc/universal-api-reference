# Umami: List Session Property Values



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-session-property-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-session-property-values?connectionId=$CONNECTION_ID&websiteId=string&startAt=1&endAt=1&propertyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1",
  "propertyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-session-property-values?${params}`, {
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
| `startAt` | number | yes | Timestamp in milliseconds for the start of the reporting range. |
| `endAt` | number | yes | Timestamp in milliseconds for the end of the reporting range. |
| `propertyName` | string | yes | Session property name to aggregate values for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number | Count of sessions with the property value. |
| `value` | string | Observed property value. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/session-data/values` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-property-values.md) for the provider-specific parameters and requirements.

