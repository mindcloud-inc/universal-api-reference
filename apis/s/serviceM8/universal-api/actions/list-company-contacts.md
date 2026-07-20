# ServiceM8: List Company Contacts



```
GET https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-company-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-company-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-company-contacts?${params}`, {
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
| `filter` | string | no | Example: `active eq 1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "companyUuid": "string",
      "editDate": "string",
      "email": "ava@example.com",
      "first": "string",
      "isPrimaryContact": "string",
      "last": "string",
      "mobile": "string",
      "phone": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `companyUuid` | string |  |
| `editDate` | string |  |
| `email` | string |  |
| `first` | string |  |
| `isPrimaryContact` | string |  |
| `last` | string |  |
| `mobile` | string |  |
| `phone` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native ServiceM8 API, this operation is `GET /api_1.0/companycontact.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-contacts.md) for the provider-specific parameters and requirements.

