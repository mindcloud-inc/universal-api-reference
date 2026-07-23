# Rillion Prime: List Accounts By Role



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-accounts-by-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-accounts-by-role?connectionId=$CONNECTION_ID&limit=25&offset=0&role=Administrator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "role": "Administrator"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-accounts-by-role?${params}`, {
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
| `role` | string | yes | Role name to use in the path, for example Administrator. Example: `Administrator`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "accountId": 1,
      "chTime": "string",
      "chUser": "string",
      "company": "string",
      "companyIsNull": 1,
      "deliveryStatus": 1,
      "favourite": true,
      "forProcessing": true,
      "index": 1,
      "inspected": true,
      "invoiceStatus": 1,
      "isAllocationsAccount": true,
      "keyValuesRowState": 1,
      "locked": true,
      "lockedRowLockedTime": "string",
      "name": "Ava Chen",
      "noteMandatory": true,
      "rowState": 1,
      "selected": true,
      "selectOption": 1,
      "useNumber": 1,
      "useObject1": 1,
      "useObject2": 1,
      "useObject3": 1,
      "useObject4": 1,
      "useObject5": 1,
      "useObject6": 1,
      "useObject7": 1,
      "useObject8": 1,
      "validTo": "string",
      "vatCodeMandatory": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `accountId` | number |  |
| `chTime` | string |  |
| `chUser` | string |  |
| `company` | string |  |
| `companyIsNull` | number |  |
| `deliveryStatus` | number |  |
| `favourite` | boolean |  |
| `forProcessing` | boolean |  |
| `index` | number |  |
| `inspected` | boolean |  |
| `invoiceStatus` | number |  |
| `isAllocationsAccount` | boolean |  |
| `keyValuesRowState` | number |  |
| `locked` | boolean |  |
| `lockedRowLockedTime` | string |  |
| `name` | string |  |
| `noteMandatory` | boolean |  |
| `rowState` | number |  |
| `selected` | boolean |  |
| `selectOption` | number |  |
| `useNumber` | number |  |
| `useObject1` | number |  |
| `useObject2` | number |  |
| `useObject3` | number |  |
| `useObject4` | number |  |
| `useObject5` | number |  |
| `useObject6` | number |  |
| `useObject7` | number |  |
| `useObject8` | number |  |
| `validTo` | string |  |
| `vatCodeMandatory` | boolean |  |

## Native endpoint

Through the native Rillion Prime API, this operation is `GET /account/role/:role` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts-by-role.md) for the provider-specific parameters and requirements.

