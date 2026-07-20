# Devin: Delete Playbook

Deletes an existing playbook from Devin.

```
DELETE https://connect.mindcloud.co/v1/universal/devin/latest/actions/delete-playbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/devin/latest/actions/delete-playbook?connectionId=$CONNECTION_ID&orgId=string&playbookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string",
  "playbookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/delete-playbook?${params}`, {
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
| `orgId` | string | yes | Devin organization ID. |
| `playbookId` | string | yes | Playbook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_type": "string",
      "body": "string",
      "created_at": 1,
      "created_by": "string",
      "macro": "string",
      "org_id": "string",
      "playbook_id": "string",
      "title": "string",
      "updated_at": 1,
      "updated_by": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_type` | string | Access scope. |
| `body` | string | Playbook body. |
| `created_at` | number | Creation timestamp. |
| `created_by` | string | Creator identifier. |
| `macro` | string | Optional playbook macro. |
| `org_id` | string | Organization ID. |
| `playbook_id` | string | Deleted playbook ID. |
| `title` | string | Playbook title. |
| `updated_at` | number | Update timestamp. |
| `updated_by` | string | Updater identifier. |

## Native endpoint

Through the native Devin API, this operation is `DELETE /v3/organizations/:org_id/playbooks/:playbook_id` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-playbook.md) for the provider-specific parameters and requirements.

