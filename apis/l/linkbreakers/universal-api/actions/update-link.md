# Linkbreakers: Update a Link

Updates an existing link in Linkbreakers.

```
PUT https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the link to update. |
| `directoryId` | string | no | The directory to move the link into. |
| `directoryIdDelete` | boolean | no | Remove the link from its directory. |
| `fallbackDestination` | string | no | Fallback destination URL to use when workflow steps are broken. |
| `leadGoalDefinition` | string | no | The lead goal definition for the link. |
| `leadTargetDefinition` | string | no | The lead target definition for the link. |
| `name` | string | no | The new name of the link. |
| `pageThemeId` | string | no | Page theme ID to assign to the link. |
| `qrcodeTemplateId` | string | no | QR code template ID to assign to the link. |
| `qrcodeTemplateIdDelete` | boolean | no | Remove the QR code template ID from the link. |
| `tags[]` | array<string> | no | Tags to associate with the link. |
| `tagsDelete` | boolean | no | Remove all tags from the link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": {
        "createdAt": "https://example.com",
        "customDomainId": "https://example.com",
        "destination": "https://example.com",
        "directoryId": "https://example.com",
        "entrypoint": "https://example.com",
        "eventCount": 1,
        "fallbackDestination": "https://example.com",
        "id": "https://example.com",
        "metadata": {},
        "name": "https://example.com",
        "qrcodeDesignId": "https://example.com",
        "qrcodeSignedUrl": "https://example.com",
        "qrcodeTemplateId": "https://example.com",
        "shortlink": "https://example.com",
        "updatedAt": "https://example.com",
        "workspaceId": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | object | Updated shortened link. |
| `link.createdAt` | string |  |
| `link.customDomainId` | string |  |
| `link.destination` | string |  |
| `link.directoryId` | string |  |
| `link.entrypoint` | string |  |
| `link.eventCount` | number |  |
| `link.fallbackDestination` | string |  |
| `link.id` | string |  |
| `link.metadata` | object |  |
| `link.name` | string |  |
| `link.qrcodeDesignId` | string |  |
| `link.qrcodeSignedUrl` | string |  |
| `link.qrcodeTemplateId` | string |  |
| `link.shortlink` | string |  |
| `link.updatedAt` | string |  |
| `link.workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `PATCH /v1/links/:id` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

