# Twilio: List Messaging Service Alpha Senders

Retrieves messaging service alpha senders from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-service-alpha-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-service-alpha-senders?connectionId=$CONNECTION_ID&limit=25&offset=0&serviceSid=%7B%7Bcredentials.twilioMessagingServiceSid%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "serviceSid": "{{credentials.twilioMessagingServiceSid}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-service-alpha-senders?${params}`, {
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
| `serviceSid` | string | yes | Default: `{{credentials.twilioMessagingServiceSid}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "firstPageUrl": "https://example.com",
        "key": "string",
        "nextPageUrl": "https://example.com",
        "page": 1,
        "pageSize": 1,
        "previousPageUrl": "https://example.com",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.firstPageUrl` | string |  |
| `meta.key` | string |  |
| `meta.nextPageUrl` | string |  |
| `meta.page` | number |  |
| `meta.pageSize` | number |  |
| `meta.previousPageUrl` | string |  |
| `meta.url` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `GET https://messaging.twilio.com/v1/Services/:ServiceSid/AlphaSenders` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messaging-service-alpha-senders.md) for the provider-specific parameters and requirements.

