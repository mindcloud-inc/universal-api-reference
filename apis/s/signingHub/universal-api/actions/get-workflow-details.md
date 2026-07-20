# SigningHub: Get Workflow Details

Retrieves workflow details from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-workflow-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-workflow-details?connectionId=$CONNECTION_ID&packageId=11191587" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "11191587"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-workflow-details?${params}`, {
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
| `packageId` | number | yes | The document package whose workflow details should be returned. Example: `11191587`. |

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

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/workflow` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-details.md) for the provider-specific parameters and requirements.

