# BambooHR: List Job Locations

Lists job locations from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-locations?${params}`, {
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
| `sort` | string | no | Ordering by OData (Open Data Protocol) v4 specification. Supported fields: label, archived, manageable, address/address1, address/address2, address/city, address/stateId, address/zipcode, address/countryId, address/timezone, address/remoteLocation, createdAt, archivedAt |
| `select` | string | no | Projection (field selection) by OData specification. Supported fields: id, label, archived, manageable, address/address1, address/address2, address/city, address/stateId, address/zipcode, address/countryId, address/timezone, address/remoteLocation, createdAt, archivedAt |
| `filter` | string | no | Filter by an OData (Open Data Protocol) v4 specification. Supported fields: id, label, archived, manageable, address/address1, address/address2, address/city, address/stateId, address/zipcode, address/countryId, address/timezone, address/remoteLocation |
| `expand` | list<string> | no | Comma-separated list of related resources to expand. Supported values: state, country. Example: expand=state,country One of: `country`, `state`. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/hris/org/locations` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-job-locations.md) for the provider-specific parameters and requirements.

