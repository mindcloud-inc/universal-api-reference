# Cerbo: Search Patients

Finds patients in Cerbo by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/search-patients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/search-patients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/search-patients?${params}`, {
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
| `last_name` | string | no | Match patients with given last name. Allows wildcard: smith% will match “Smith”,”Smithson”,”Simthe” etc) |
| `first_name` | string | no | Match patients with given first name Allows wildcard: ben% will match “Ben”,”Benjamin”,”Bennett” etc) |
| `email` | string | no | Match patients with given email as their primary or secondary address Allows wildcard: %@gmail.com will match all patients with Gmail addresses |
| `username` | string | no | Match patients with given patient portal username |
| `dob` | string | no | Match patients with given date of birth (preferred format is yyyy-mmdd). No wildcards allowed |
| `timezone` | string | no | Match patients with given timezone (Must be a canonical timezone https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `GET /patients/search` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-patients.md) for the provider-specific parameters and requirements.

