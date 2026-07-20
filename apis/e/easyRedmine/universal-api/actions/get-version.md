# Easy Redmine: Get Version

Retrieves a version from Easy Redmine.

```
GET https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/get-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Redmine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/get-version?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/get-version?${params}`, {
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
| `id` | number | yes | ID of the version to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "project": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `dueDate` | date |  |
| `effectiveDate` | date |  |
| `id` | number |  |
| `name` | string |  |
| `project` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Easy Redmine API, this operation is `GET /versions/:id.json` (base URL `https://3f73561b8b.bigus-e5.easy8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-version.md) for the provider-specific parameters and requirements.

