# Aspire: List Addresses



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-addresses?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressID": 1,
      "addressLine1": {},
      "addressLine2": {},
      "city": {},
      "createdByUserId": 1,
      "createdByUserName": "Ava Chen",
      "createdOn": "string",
      "lastModifiedByUserId": {},
      "lastModifiedByUserName": {},
      "lastModifiedOn": {},
      "stateProvinceCode": {},
      "zipCode": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressID` | number |  |
| `addressLine1` | object |  |
| `addressLine2` | object |  |
| `city` | object |  |
| `createdByUserId` | number |  |
| `createdByUserName` | string |  |
| `createdOn` | string |  |
| `lastModifiedByUserId` | object |  |
| `lastModifiedByUserName` | object |  |
| `lastModifiedOn` | object |  |
| `stateProvinceCode` | object |  |
| `zipCode` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Addresses` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.

