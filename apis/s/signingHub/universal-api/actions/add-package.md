# SigningHub: Add Package

Creates a package in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-package', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageName` | string | no | The name of the package. Defaults to Untitled when omitted. Example: `Customer NDA Package`. |
| `workflowMode` | string | no | Controls whether the workflow is for me only, others only, or me and others. Default: `ME_AND_OTHERS`. |
| `folderName` | string | no | Optional folder name to upload the package into an existing custom or shared folder. Example: `Legal Intake`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "package_id": 1,
      "workflow_mode": "string",
      "workflow_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `package_id` | number |  |
| `workflow_mode` | string |  |
| `workflow_type` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-package.md) for the provider-specific parameters and requirements.

