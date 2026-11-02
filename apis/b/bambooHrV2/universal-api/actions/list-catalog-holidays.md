# BambooHR: List Catalog Holidays

Lists catalog holidays from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-catalog-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-catalog-holidays?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-catalog-holidays?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryCode` | string | no | ISO 3166-1 alpha-2 country code. Filters the catalog to entries for the given country. |
| `year` | number | no | Calendar year. Filters the catalog to entries whose startDate falls in the given year. |
| `filter` | string | no | OData v4 filter expression. Supported fields: name, type, countryCode, startDate. Example: startDate ge '2026-01-01' and type eq 'PUBLIC' |
| `orderBy` | string | no | Sort expression. Allowed fields: startDate, name, with optional asc/desc direction. Default: `startDate asc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/holidays/catalog` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-catalog-holidays.md) for the provider-specific parameters and requirements.

