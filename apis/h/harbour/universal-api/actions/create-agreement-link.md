# Harbour: Create Agreement Link

Creates a new agreement link in Harbour.

```
POST https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-agreement-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-agreement-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agreement_id": "AGREE-AbCd1234",
  "destination_folder_id": "folder-AbCd1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-agreement-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agreement_id": "AGREE-AbCd1234",
    "destination_folder_id": "folder-AbCd1234"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agreement_id` | string | yes | Agreement template identifier used to create the link. Example: `AGREE-AbCd1234`. |
| `request_title` | string | no | Title shown in the Harbour signature page. Example: `Agreement`. |
| `destination_folder_id` | string | yes | Folder where the completed agreement will be saved. Example: `folder-AbCd1234`. |
| `auth_mode` | string | no | Authentication mode: PASSCODE, EMAILS, or PUBLIC. Example: `PUBLIC`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `brand_id` | string | no | Brand identifier for the agreement link. Example: `BRAND-AbCd1234`. |
| `passcode` | string | no | Passcode value when auth_mode is PASSCODE. Example: `1234`. |
| `recipients[]` | array<object> | no | Array of recipient objects when auth_mode is EMAILS. |
| `is_active` | boolean | no | Whether the generated agreement link is active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agreement_link": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreement_link` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `POST https://api.harbourshare.com/v1/agreement_links` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agreement-link.md) for the provider-specific parameters and requirements.

