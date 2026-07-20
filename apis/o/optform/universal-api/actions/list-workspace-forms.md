# Optform: List Workspace Forms

Retrieves forms from a specific Optform workspace.

```
GET https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-workspace-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-workspace-forms?connectionId=$CONNECTION_ID&workspaceId=4ff18535-b33d-4729-999a-85b7eb080530" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "4ff18535-b33d-4729-999a-85b7eb080530"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-workspace-forms?${params}`, {
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
| `workspaceId` | string | yes | Example: `4ff18535-b33d-4729-999a-85b7eb080530`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundColor": "string",
      "buttonColor": "string",
      "buttonTextColor": "string",
      "coverImageUrl": "https://example.com",
      "description": "string",
      "id": "string",
      "mainTextColor": "string",
      "name": "Ava Chen",
      "status": "string",
      "theme": "string",
      "themeVersion": 1,
      "type": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundColor` | string |  |
| `buttonColor` | string |  |
| `buttonTextColor` | string |  |
| `coverImageUrl` | string |  |
| `description` | string |  |
| `id` | string |  |
| `mainTextColor` | string |  |
| `name` | string |  |
| `status` | string |  |
| `theme` | string |  |
| `themeVersion` | number |  |
| `type` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Optform API, this operation is `GET /api/Form/all/:workspaceId` (base URL `https://optform.azure-api.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-forms.md) for the provider-specific parameters and requirements.

