# Modern Treasury: List Internal Accounts

Retrieves internal accounts from Modern Treasury.

```
GET https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-internal-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modern Treasury `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-internal-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-internal-accounts?${params}`, {
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
| `currency` | string | no | Only return internal accounts with this currency. Example: `USD`. |
| `status` | list<string> | no | Only return internal accounts with this status. One of: `0`, `1`, `2`, `3`, `4`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `counterpartyId` | string | no | Only return internal accounts associated with this counterparty. |
| `legalEntityId` | string | no | Only return internal accounts associated with this legal entity. |
| `paymentType` | string | no | Only return internal accounts that can make this type of payment. Example: `ach`. |
| `paymentDirection` | list<string> | no | Only return internal accounts that can originate payments with this direction. One of: `0`, `1`. |
| `externalId` | string | no | Only return internal accounts with this user-defined external ID. |
| `metadata` | string | no | Metadata filter using Modern Treasury's metadata query format. Example: `metadata[Type]=Loan`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountCapabilities": {},
      "accountDetails": [
        {}
      ],
      "accountType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "liveMode": true,
      "name": "Ava Chen",
      "object": "string",
      "partyAddress": {},
      "partyName": "Ava Chen",
      "partyType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountCapabilities` | object |  |
| `accountDetails` | array<object> |  |
| `accountType` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `liveMode` | boolean |  |
| `name` | string |  |
| `object` | string |  |
| `partyAddress` | object |  |
| `partyName` | string |  |
| `partyType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Modern Treasury API, this operation is `GET /internal_accounts` (base URL `https://app.moderntreasury.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-internal-accounts.md) for the provider-specific parameters and requirements.

