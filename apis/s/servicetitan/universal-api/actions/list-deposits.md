# ServiceTitan: List Deposits

Retrieves bank deposits and their accounting details from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-deposits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-deposits?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-deposits?${params}`, {
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
| `ids` | string | no | Deposit IDs to retrieve, up to 50 IDs. Accepts multiple values in one string, delimited by `,`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modifiedBefore` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `modifiedOnOrAfter` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `createdBefore` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `createdOnOrAfter` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `depositDateBefore` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `depositDateOnOrAfter` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `reviewedBefore` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `reviewedOnOrAfter` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `reviewStatus` | list<string> | no | One of: `NeedsReview`, `Reviewed`. |
| `depositStatus` | list<string> | no | One of: `Deposited`, `Open`, `Undefined`. |
| `syncStatus` | list<string> | no | One of: `Exported`, `Pending`, `Posted`. |
| `grossAmountGreater` | number | no |  |
| `grossAmountLess` | number | no |  |
| `includeTotal` | boolean | no |  |
| `sort` | string | no | Prefix a supported field name with + for ascending order or - for descending order. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET accounting/v2/tenant/{{credentials.tenant}}/bank-deposits` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deposits.md) for the provider-specific parameters and requirements.

