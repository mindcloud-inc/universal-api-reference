# Klenty: List Prospects By Created Date

Retrieves prospects from Klenty by created date.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-created-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-created-date?connectionId=$CONNECTION_ID&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-created-date?${params}`, {
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
| `startDate` | string | yes | Start date in YYYY/MM/DD format. |
| `endDate` | string | no | End date in YYYY/MM/DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignTo": "string",
      "company": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "list": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignTo` | string |  |
| `company` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `list` | string |  |

## Native endpoint

Through the native Klenty API, this operation is `GET /prospects` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prospects-by-created-date.md) for the provider-specific parameters and requirements.

