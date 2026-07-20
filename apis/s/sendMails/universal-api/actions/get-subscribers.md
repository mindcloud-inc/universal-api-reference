# SendMails: Get Subscribers

Retrieves a list of subscribers from SendMails.

```
GET https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-subscribers?connectionId=$CONNECTION_ID&listUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-subscribers?${params}`, {
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
| `listUid` | string | yes | List UID from SendMails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "ipAddress": "string",
      "listUid": "string",
      "source": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Subscriber email address. |
| `id` | number | Subscriber numeric ID. |
| `ipAddress` | string | Subscriber IP address. |
| `listUid` | string | Owning list UID. |
| `source` | string | Subscriber source. |
| `status` | string | Subscription status. |

## Native endpoint

Through the native SendMails API, this operation is `GET /subscribers` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscribers.md) for the provider-specific parameters and requirements.

