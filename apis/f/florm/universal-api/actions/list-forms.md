# Florm: List Forms

Retrieves forms from your Florm workspace.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-forms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `guid` | string | GUID of the Florm form. |
| `settings` | object | Form settings object. |
| `sharedGuid` | string | Shared GUID of the form when present. |
| `slug` | string | Form slug. |
| `steps` | array<object> | Form step definitions. |
| `updatedAt` | string | Last update timestamp. |
| `urlParameters` | object | URL parameter configuration. |
| `version` | number | Saved form version when present. |
| `workspaceGuid` | string | GUID of the owning workspace. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/forms/` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

