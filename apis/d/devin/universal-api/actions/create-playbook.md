# Devin: Create Playbook

Creates a new playbook in Devin.

```
POST https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-playbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-playbook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "orgId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-playbook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "orgId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | Playbook body/instructions. |
| `macro` | string | no | Optional playbook macro identifier such as !my_macro. |
| `orgId` | string | yes | Devin organization ID. |
| `title` | string | yes | Playbook title. |

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
| `playbook_id` | string | Playbook ID. |
| `title` | string | Playbook title. |
| `updated_at` | number | Update timestamp. |
| `updated_by` | string | Updater identifier. |

## Native endpoint

Through the native Devin API, this operation is `POST /v3/organizations/:org_id/playbooks` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-playbook.md) for the provider-specific parameters and requirements.

