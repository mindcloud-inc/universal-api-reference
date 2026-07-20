# MailerCheck: Get Verification List

Retrieves a verification list from MailerCheck.

```
GET https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-verification-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-verification-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-verification-list?${params}`, {
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
| `id` | number | yes | Verification list identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "source": "string",
      "statistics": {},
      "status": {},
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "verificationEnded": "2026-05-07T12:00:00.000Z",
      "verificationStarted": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `count` | number |  |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `source` | string |  |
| `statistics` | object |  |
| `status` | object |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `verificationEnded` | date |  |
| `verificationStarted` | date |  |

## Native endpoint

Through the native MailerCheck API, this operation is `GET /lists/:id` (base URL `https://app.mailercheck.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-list.md) for the provider-specific parameters and requirements.

