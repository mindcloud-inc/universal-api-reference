# HigherGov: List Grant Programs

Retrieves grant programs from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-grant-programs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-grant-programs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-grant-programs?${params}`, {
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
| `agencyKey` | string | no | HigherGov Agency key |
| `cfdaProgramNumber` | string | no | CFDA program number for the grant program |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "cfda_objective": "string",
      "cfda_program_number": "string",
      "date_modified": "string",
      "path": "string",
      "popular_program_title": "string",
      "primary_agency": {},
      "program_title": "string",
      "type_of_assistance": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `cfda_objective` | string |  |
| `cfda_program_number` | string |  |
| `date_modified` | string |  |
| `path` | string |  |
| `popular_program_title` | string |  |
| `primary_agency` | object |  |
| `program_title` | string |  |
| `type_of_assistance` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/grant-program/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-grant-programs.md) for the provider-specific parameters and requirements.

