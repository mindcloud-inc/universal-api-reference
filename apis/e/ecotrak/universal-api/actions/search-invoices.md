# Ecotrak: Search Invoices

Finds invoices in Ecotrak by approved or created date.

```
GET https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/search-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecotrak `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/search-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/search-invoices?${params}`, {
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
| `approvedDate` | string | no | The date for which approved invoices are to be searched. Format YYYY-MM-DD. |
| `excludeLocationTypeId` | number | no | The ID of the location type to be excluded from the search. |
| `createdAt` | string | no | The date for which invoices were created. Format YYYY-MM-DD. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecotrak API returns.

## Native endpoint

Through the native Ecotrak API, this operation is `GET /v1/invoices/search` (base URL `https://api.ecotrak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-invoices.md) for the provider-specific parameters and requirements.

