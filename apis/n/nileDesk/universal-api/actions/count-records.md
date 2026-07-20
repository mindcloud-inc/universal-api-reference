# NileDesk: Count Records

Counts matching records in NileDesk by filters.

```
GET https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/count-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NileDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/count-records?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/count-records?${params}`, {
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
| `filters` | object | no | Optional NileDesk filter object, for example {"logic":"and","rules":[{"field1":"value","operator":"eq"}]}. |
| `process_id` | string | no | Optional process or board item identifier to narrow the count. |
| `template_id` | string | yes | The NileDesk template to count records from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
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
| `count` | number | The count returned by NileDesk. |
| `message` | string | Provider message describing the result. |
| `success` | boolean | Whether NileDesk accepted the request. |

## Native endpoint

Through the native NileDesk API, this operation is `POST /CountRecords` (base URL `https://app.niledesk.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-records.md) for the provider-specific parameters and requirements.

