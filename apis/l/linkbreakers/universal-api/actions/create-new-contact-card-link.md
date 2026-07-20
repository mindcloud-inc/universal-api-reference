# Linkbreakers: Create a New Contact Card Link

Creates a new contact card link in Linkbreakers.

```
POST https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-new-contact-card-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-new-contact-card-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vcardData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-new-contact-card-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vcardData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customDomainId` | string | no | The custom domain ID. |
| `fallbackDestination` | string | no | Optional fallback URL if vCard download fails. |
| `leadGoalDefinition` | string | no | The lead goal definition for the link. |
| `leadTargetDefinition` | string | no | The lead target definition for the link. |
| `metadata` | object | no | Map of string key-value metadata for the contact link. |
| `name` | string | no | The name of the link. |
| `qrcodeDesignId` | string | no | The QR code design ID. |
| `qrcodeTemplateId` | string | no | The QR code template ID. |
| `shortlink` | string | no | The shortlink slug for the link. |
| `tags[]` | array<string> | no | Tags to associate with the link. |
| `vcardData` | object | yes | Contact information payload for the vCard link. |
| `waitForQrcode` | boolean | no | Wait for QR code generation to complete. |

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
| `link` | object | Created contact-card link. |
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

Through the native Linkbreakers API, this operation is `POST /v1/links/contact` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-contact-card-link.md) for the provider-specific parameters and requirements.

