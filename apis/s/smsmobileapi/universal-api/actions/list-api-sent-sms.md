# Smsmobileapi: List API Sent SMS

Retrieves SMS messages sent through Smsmobileapi.

```
GET https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-api-sent-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smsmobileapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-api-sent-sms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-api-sent-sms?${params}`, {
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
| `guid_message` | string | no | Filter the log to one exact SMS GUID. |
| `keyword` | string | no | Filter by recipient number or message content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `error_api` | list | no | Only return SMS entries that have an API request error. One of: `1`. |
| `error_mobile` | list | no | Only return SMS entries that have a mobile processing error. One of: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Provider envelope containing the API SMS log result, including the error code and SMS entries array. |

## Native endpoint

Through the native Smsmobileapi API, this operation is `GET /log/sent/sms/` (base URL `https://api.smsmobileapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-sent-sms.md) for the provider-specific parameters and requirements.

