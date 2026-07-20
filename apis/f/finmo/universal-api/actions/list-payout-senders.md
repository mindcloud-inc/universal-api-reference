# Finmo: List Payout Senders

Retrieves payout senders from the Finmo platform.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payout-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payout-senders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payout-senders?${params}`, {
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
| `payoutSenderId` | string | no |  |
| `type` | string | no |  |
| `senderName` | string | no |  |
| `email` | string | no |  |
| `organizationReferenceId` | string | no |  |
| `addressLine1` | string | no |  |
| `addressLine2` | string | no |  |
| `addressCity` | string | no |  |
| `addressState` | string | no |  |
| `addressCountry` | string | no |  |
| `addressZipCode` | string | no |  |
| `phoneNumber` | string | no |  |
| `phoneCountryCode` | string | no |  |
| `phoneNumberE164` | string | no |  |
| `description` | string | no |  |
| `isActive` | boolean | no |  |
| `createdAt` | string | no |  |
| `limit` | number | no |  |
| `page` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "createdAt": "string",
      "currency": "string",
      "description": "string",
      "individual": {},
      "isActive": true,
      "metadata": {},
      "orgId": "string",
      "payoutSenderId": "string",
      "senderName": "Ava Chen",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `individual` | object |  |
| `isActive` | boolean |  |
| `metadata` | object |  |
| `orgId` | string |  |
| `payoutSenderId` | string |  |
| `senderName` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /payout-sender` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payout-senders.md) for the provider-specific parameters and requirements.

