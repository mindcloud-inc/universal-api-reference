# SigningHub: Start New Workflow From Existing Package

Creates a new workflow from an existing package in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/start-new-workflow-from-existing-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/start-new-workflow-from-existing-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191524"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/start-new-workflow-from-existing-package', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191524"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | Package ID of the existing document package. Example: `11191524`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "folder": "string",
      "folder_id": 1,
      "gatekeeper": true,
      "modified_on": "string",
      "next_signer": "string",
      "next_signer_email": [
        {}
      ],
      "owner_name": "Ava Chen",
      "package_id": 1,
      "package_name": "Ava Chen",
      "package_owner": "string",
      "package_status": "string",
      "shared_package": true,
      "uploaded_on": "string",
      "users": [
        {}
      ],
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> |  |
| `folder` | string |  |
| `folder_id` | number |  |
| `gatekeeper` | boolean |  |
| `modified_on` | string |  |
| `next_signer` | string |  |
| `next_signer_email` | array<object> |  |
| `owner_name` | string |  |
| `package_id` | number |  |
| `package_name` | string |  |
| `package_owner` | string |  |
| `package_status` | string |  |
| `shared_package` | boolean |  |
| `uploaded_on` | string |  |
| `users` | array<object> |  |
| `workflow` | object |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/workflow/new` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-new-workflow-from-existing-package.md) for the provider-specific parameters and requirements.

