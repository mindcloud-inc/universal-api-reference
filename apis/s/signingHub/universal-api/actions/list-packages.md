# SigningHub: List Packages

Retrieves packages from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-packages?connectionId=$CONNECTION_ID&documentStatus=ALL&pageNo=1&recordPerPage=20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentStatus": "ALL",
  "pageNo": "1",
  "recordPerPage": "20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-packages?${params}`, {
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
| `documentStatus` | string | yes | Package status filter, for example ALL or DRAFT. Default: `ALL`. Example: `ALL`. |
| `pageNo` | number | yes | Page number according to the division of records per page. Default: `1`. Example: `1`. |
| `recordPerPage` | number | yes | Number of packages to fetch per request. Default: `20`. Example: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": "string",
      "modified_on": "2026-05-07T12:00:00.000Z",
      "package_id": 1,
      "package_name": "Ava Chen",
      "package_status": "string",
      "size": 1,
      "uploaded_on": "2026-05-07T12:00:00.000Z",
      "workflow_mode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | string |  |
| `modified_on` | date |  |
| `package_id` | number |  |
| `package_name` | string |  |
| `package_status` | string |  |
| `size` | number |  |
| `uploaded_on` | date |  |
| `workflow_mode` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:document_status/:pageNo/:recordPerPage` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-packages.md) for the provider-specific parameters and requirements.

