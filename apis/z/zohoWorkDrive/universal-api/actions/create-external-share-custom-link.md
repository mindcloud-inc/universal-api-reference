# Zoho WorkDrive: Create External Share Custom Link

Creates an external share link in Zoho WorkDrive.

```
POST https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/create-external-share-custom-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho WorkDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/create-external-share-custom-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.resourceId": "string",
  "data.attributes.linkName": "https://example.com",
  "data.attributes.requestUserData": true,
  "data.attributes.allowDownload": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/create-external-share-custom-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.resourceId": "string",
    "data.attributes.linkName": "https://example.com",
    "data.attributes.requestUserData": true,
    "data.attributes.allowDownload": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.attributes.resourceId` | string | yes | The file or folder resource ID to share. |
| `data.attributes.linkName` | string | yes | Display name for the external share link. |
| `data.attributes.requestUserData` | boolean | yes | Whether the recipient must submit contact information before access. |
| `data.attributes.allowDownload` | boolean | yes | Whether recipients can download the shared resource. |
| `data.attributes.passwordText` | string | no | Optional password that protects the share link. |
| `data.attributes.inputFields` | list | no | Optional list of custom recipient fields to collect before access. |
| `data.attributes.roleId` | number | no | Optional role ID that controls the shared permission level. |
| `data.attributes.expirationDate` | string | no | Optional link expiration date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Provider resource attributes. |
| `id` | string | Resource ID. |
| `links` | object | Provider self and related links. |
| `relationships` | object | Provider relationship links. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Zoho WorkDrive API, this operation is `POST /api/v1/links` (base URL `{{credentials.accessTokenRequest.api_domain}}/workdrive`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-external-share-custom-link.md) for the provider-specific parameters and requirements.

