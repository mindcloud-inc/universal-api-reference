# SureCart: Update Account



```
PUT https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account.name` | string | no | The account display name. Example: `My Store`. |
| `account.currency` | string | no | The default currency for the account. Example: `usd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "currency": "string",
      "currencyLocked": true,
      "id": "string",
      "locale": "string",
      "name": "Ava Chen",
      "object": "string",
      "publicToken": "string",
      "slug": "string",
      "timeZone": "string",
      "updatedAt": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `currency` | string |  |
| `currencyLocked` | boolean |  |
| `id` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `object` | string |  |
| `publicToken` | string |  |
| `slug` | string |  |
| `timeZone` | string |  |
| `updatedAt` | number |  |
| `url` | string |  |

## Native endpoint

Through the native SureCart API, this operation is `PATCH v1/account` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

