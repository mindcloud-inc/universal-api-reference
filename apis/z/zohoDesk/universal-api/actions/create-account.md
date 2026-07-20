# Zoho Desk: Create Account



```
POST https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountName` | string | yes | Name of the new account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "website": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string |  |
| `createdTime` | date |  |
| `email` | string |  |
| `id` | string |  |
| `modifiedTime` | date |  |
| `phone` | string |  |
| `website` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `POST /accounts` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

