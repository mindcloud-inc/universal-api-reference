# Zoho WorkDrive: Add Label to File/Folder

Adds a label to a Zoho WorkDrive file or folder.

```
POST https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/add-label-to-file-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho WorkDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/add-label-to-file-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "labelId": "string",
  "data[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/add-label-to-file-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "labelId": "string",
    "data[].id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `labelId` | string | yes | The label ID to assign. |
| `data[].id` | string | yes | The resource ID to associate with the label. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[].attributes.resourceId` | string | no | Optional nested resource ID field from the published WorkDrive example payload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho WorkDrive API returns.

## Native endpoint

Through the native Zoho WorkDrive API, this operation is `POST /api/v1/labels/:labelId/relationships/files` (base URL `{{credentials.accessTokenRequest.api_domain}}/workdrive`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-label-to-file-folder.md) for the provider-specific parameters and requirements.

