# Planfix: Update Project

Updates an existing project in Planfix.

```
PUT https://connect.mindcloud.co/v1/universal/planfix/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planfix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planfix/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planfix/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Planfix project identifier. |
| `name` | string | no | Updated project name. |
| `description` | string | no | Updated project description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native Planfix API, this operation is `POST /project/:id` (base URL `{{credentials.accountBaseUrl}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

