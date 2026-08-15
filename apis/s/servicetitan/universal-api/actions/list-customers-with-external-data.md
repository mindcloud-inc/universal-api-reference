# ServiceTitan: List Customers With External Data



```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-customers-with-external-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-customers-with-external-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-customers-with-external-data?${params}`, {
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
| `city` | string | no |  |
| `country` | string | no |  |
| `phone` | string | no |  |
| `state` | string | no |  |
| `unit` | string | no |  |
| `name` | string | no |  |
| `modifiedOnOrAfter` | string | no |  |
| `street` | string | no |  |
| `zip` | string | no |  |
| `createdOnOrAfter` | string | no |  |
| `active` | boolean | no |  |
| `ids` | string | no |  |
| `excludeAccountingChangesFromModifiedDateRange` | boolean | no | Excludes accounting changes such as balance adjustments from the modified date range. |
| `externalDataApplicationGuid` | string | no | Returns customer records with external data for this application GUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET crm/v2/tenant/{{credentials.tenant}}/customers` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers-with-external-data.md) for the provider-specific parameters and requirements.

