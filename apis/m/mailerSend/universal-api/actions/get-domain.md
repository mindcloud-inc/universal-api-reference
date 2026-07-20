# MailerSend: Get Domain



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain?connectionId=$CONNECTION_ID&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain?${params}`, {
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
| `domainId` | string | yes | ID of the MailerSend domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "dkim": true,
      "domainSettings": {},
      "domainStats": {},
      "hasNotQueuedMessages": true,
      "id": "string",
      "isCnameActive": true,
      "isCnameVerified": true,
      "isDnsActive": true,
      "isTrackingAllowed": true,
      "isVerified": true,
      "name": "Ava Chen",
      "notQueuedMessagesCount": 1,
      "spf": true,
      "totals": [
        {}
      ],
      "tracking": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `dkim` | boolean |  |
| `domainSettings` | object |  |
| `domainStats` | object |  |
| `hasNotQueuedMessages` | boolean |  |
| `id` | string |  |
| `isCnameActive` | boolean |  |
| `isCnameVerified` | boolean |  |
| `isDnsActive` | boolean |  |
| `isTrackingAllowed` | boolean |  |
| `isVerified` | boolean |  |
| `name` | string |  |
| `notQueuedMessagesCount` | number |  |
| `spf` | boolean |  |
| `totals` | array<object> |  |
| `tracking` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native MailerSend API, this operation is `GET /domains/:domain_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

