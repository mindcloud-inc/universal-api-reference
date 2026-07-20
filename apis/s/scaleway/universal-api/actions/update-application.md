# Scaleway: Update Application

Updates an existing application in Scaleway.

```
PUT https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "applicationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-application', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "applicationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `applicationId` | string | yes |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "deletable": true,
      "description": "string",
      "editable": true,
      "id": "string",
      "managed": true,
      "name": "Ava Chen",
      "nb_api_keys": 1,
      "organization_id": "string",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `deletable` | boolean |  |
| `description` | string |  |
| `editable` | boolean |  |
| `id` | string |  |
| `managed` | boolean |  |
| `name` | string |  |
| `nb_api_keys` | number |  |
| `organization_id` | string |  |
| `tags` | array<string> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Scaleway API, this operation is `PATCH /iam/v1alpha1/applications/:application_id` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-application.md) for the provider-specific parameters and requirements.

