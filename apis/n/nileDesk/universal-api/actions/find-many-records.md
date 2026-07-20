# NileDesk: Find Many Records

Finds multiple records in NileDesk by filters.

```
GET https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/find-many-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NileDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/find-many-records?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/find-many-records?${params}`, {
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
| `fields[]` | array<string> | no | Optional list of field keys to return. Leave empty to return all fields. |
| `filters` | object | no | Optional NileDesk filter object, for example {"logic":"and","rules":[{"field1":"value","operator":"eq"}]}. |
| `limit` | number | no | Optional maximum number of records to return. |
| `process_id` | string | no | Optional process or board item identifier to narrow the search. |
| `sort` | object | no | Optional NileDesk sort object, for example {"field":"_id","sort_by":"desc"}. |
| `template_id` | string | yes | The NileDesk template to query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | The records returned by NileDesk. |
| `message` | string | Provider message describing the result. |
| `success` | boolean | Whether NileDesk accepted the request. |

## Native endpoint

Through the native NileDesk API, this operation is `POST /FindManyRecord` (base URL `https://app.niledesk.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-many-records.md) for the provider-specific parameters and requirements.

