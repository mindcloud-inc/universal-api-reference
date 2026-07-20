# Scaleway: Get Group

Retrieves a group from Scaleway.

```
GET https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-group?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-group?${params}`, {
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
| `groupId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application_ids": [
        "string"
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "deletable": true,
      "description": "string",
      "editable": true,
      "id": "string",
      "managed": true,
      "name": "Ava Chen",
      "organization_id": "string",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application_ids` | array<string> |  |
| `created_at` | date |  |
| `deletable` | boolean |  |
| `description` | string |  |
| `editable` | boolean |  |
| `id` | string |  |
| `managed` | boolean |  |
| `name` | string |  |
| `organization_id` | string |  |
| `tags` | array<string> |  |
| `updated_at` | date |  |
| `user_ids` | array<string> |  |

## Native endpoint

Through the native Scaleway API, this operation is `GET /iam/v1alpha1/groups/:group_id` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

