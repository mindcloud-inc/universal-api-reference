# Channels: Get Number Do Not Call History

Retrieves do-not-call history for a phone number in Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-number-do-not-call-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-number-do-not-call-history?connectionId=$CONNECTION_ID&msisdn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "msisdn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-number-do-not-call-history?${params}`, {
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
| `msisdn` | string | yes | Phone number whose Do Not Call List history should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "eventDate": "2026-05-07T12:00:00.000Z",
          "msisdn": "string",
          "status": "string",
          "userId": 1,
          "username": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].eventDate` | date |  |
| `[].msisdn` | string |  |
| `[].status` | string |  |
| `[].userId` | number |  |
| `[].username` | string |  |

## Native endpoint

Through the native Channels API, this operation is `GET /api/v1/dnclist/{msisdn}` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-number-do-not-call-history.md) for the provider-specific parameters and requirements.

