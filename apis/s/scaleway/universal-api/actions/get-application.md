# Scaleway: Get Application

Retrieves an application from Scaleway.

```
GET https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-application?connectionId=$CONNECTION_ID&applicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-application?${params}`, {
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
| `applicationId` | string | yes |  |

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

Through the native Scaleway API, this operation is `GET /iam/v1alpha1/applications/:application_id` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application.md) for the provider-specific parameters and requirements.

