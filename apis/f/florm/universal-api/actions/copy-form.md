# Florm: Copy Form

Creates a copy of a Florm form.

```
POST https://connect.mindcloud.co/v1/universal/florm/latest/actions/copy-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/florm/latest/actions/copy-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/florm/latest/actions/copy-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formGuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formGuid` | string | yes | GUID of the Florm form to copy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "designThemeGuid": "string",
      "guid": "string",
      "settings": {},
      "sharedGuid": "string",
      "slug": "string",
      "steps": [
        {}
      ],
      "updatedAt": "string",
      "urlParameters": {},
      "version": 1,
      "workspaceGuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `designThemeGuid` | string | GUID of the design theme. |
| `guid` | string | GUID of the copied Florm form. |
| `settings` | object | Form settings object. |
| `sharedGuid` | string | Shared GUID of the copied form when present. |
| `slug` | string | Form slug. |
| `steps` | array<object> | Form step definitions. |
| `updatedAt` | string | Last update timestamp. |
| `urlParameters` | object | URL parameter configuration. |
| `version` | number | Saved form version when present. |
| `workspaceGuid` | string | GUID of the owning workspace. |

## Native endpoint

Through the native Florm API, this operation is `POST /v1/forms/:form_guid/copy` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-form.md) for the provider-specific parameters and requirements.

