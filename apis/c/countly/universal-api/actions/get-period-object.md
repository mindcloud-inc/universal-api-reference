# Countly: Get Period Object

Retrieves the period object from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-period-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-period-object?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-period-object?${params}`, {
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
| `appId` | string | yes | Countly app ID to query analytics for. |
| `period` | string | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, hour, or day. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Countly period object keyed by date or period bucket. |

## Native endpoint

Through the native Countly API, this operation is `GET /o` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-period-object.md) for the provider-specific parameters and requirements.

