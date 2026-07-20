# Tricentis qTest: List Projects

Retrieves available projects from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-projects?${params}`, {
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
| `expand` | string | no | Optional expansion, such as userprofile, to include profile and permission data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "sample": true,
      "start_date": "2026-05-07T12:00:00.000Z",
      "status_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `end_date` | date |  |
| `id` | number |  |
| `name` | string |  |
| `sample` | boolean |  |
| `start_date` | date |  |
| `status_id` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

