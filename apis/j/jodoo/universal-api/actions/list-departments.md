# Jodoo: List Departments



```
GET https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-departments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-departments?connectionId=$CONNECTION_ID&deptNo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deptNo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-departments?${params}`, {
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
| `deptNo` | number | yes | Department number to retrieve child departments from recursively. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deptNo": 1,
      "name": "Ava Chen",
      "parentNo": 1,
      "status": 1,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deptNo` | number |  |
| `name` | string |  |
| `parentNo` | number |  |
| `status` | number |  |
| `type` | number |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST /corp/department/list` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-departments.md) for the provider-specific parameters and requirements.

