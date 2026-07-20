# Poodll: Get Course Groups

Retrieves groups from a Poodll course.

```
GET https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-course-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poodll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-course-groups?connectionId=$CONNECTION_ID&courseid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-course-groups?${params}`, {
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
| `courseid` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "courseid": 1,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "participation": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `courseid` | number |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `participation` | boolean |  |

## Native endpoint

Through the native Poodll API, this operation is `POST {{credentials.baseUrl}}/webservice/rest/server.php` (base URL `{{credentials.baseUrl}}/webservice/rest/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course-groups.md) for the provider-specific parameters and requirements.

