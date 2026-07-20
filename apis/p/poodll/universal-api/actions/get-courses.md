# Poodll: Get Courses

Retrieves course records from Poodll.

```
GET https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poodll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-courses?${params}`, {
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
| `options` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryid": 1,
      "displayname": "Ava Chen",
      "fullname": "Ava Chen",
      "id": 1,
      "shortname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryid` | number |  |
| `displayname` | string |  |
| `fullname` | string |  |
| `id` | number |  |
| `shortname` | string |  |

## Native endpoint

Through the native Poodll API, this operation is `POST {{credentials.baseUrl}}/webservice/rest/server.php` (base URL `{{credentials.baseUrl}}/webservice/rest/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-courses.md) for the provider-specific parameters and requirements.

