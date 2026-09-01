# Zenoti: List Employees



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0&centerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "centerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-employees?${params}`, {
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
| `centerId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "id": "string",
      "jobInfo": {
        "id": "string",
        "name": "Ava Chen"
      },
      "personalInfo": {
        "firstName": "Ava",
        "gender": 1,
        "lastName": "Chen",
        "name": "Ava Chen",
        "userName": "ava@example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `id` | string |  |
| `jobInfo.id` | string |  |
| `jobInfo.name` | string |  |
| `personalInfo.firstName` | string |  |
| `personalInfo.gender` | number |  |
| `personalInfo.lastName` | string |  |
| `personalInfo.name` | string |  |
| `personalInfo.userName` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET centers/:centerId/employees` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

