# CraftMyPDF: Create editor session

Creates an editor session in CraftMyPDF.

```
POST https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-editor-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-editor-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "expiration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-editor-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "expiration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes |  |
| `expiration` | number | yes |  |
| `canSave` | boolean | no |  |
| `canCreatePDF` | boolean | no |  |
| `canViewSettings` | boolean | no |  |
| `canPreview` | boolean | no |  |
| `canEditJSON` | boolean | no |  |
| `canShowHeader` | boolean | no |  |
| `canShowLayers` | boolean | no |  |
| `canShowPropertyPanel` | boolean | no |  |
| `canShowHelp` | boolean | no |  |
| `canShowData` | boolean | no |  |
| `canShowExpressionDoc` | boolean | no |  |
| `canShowPropertyBinding` | boolean | no |  |
| `canShowBackURL` | boolean | no |  |
| `jsonMode` | number | no |  |
| `backURL` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expireAfter": "2026-05-07T12:00:00.000Z",
      "expireAfterUnixTimestamp": 1,
      "status": "string",
      "tokenUuid": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expireAfter` | date |  |
| `expireAfterUnixTimestamp` | number |  |
| `status` | string |  |
| `tokenUuid` | string |  |
| `url` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /create-editor-session` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-editor-session.md) for the provider-specific parameters and requirements.

