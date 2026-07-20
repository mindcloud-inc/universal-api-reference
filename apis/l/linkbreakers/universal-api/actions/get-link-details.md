# Linkbreakers: Get Link Details

Retrieves detailed link information from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/get-link-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/get-link-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/get-link-details?${params}`, {
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
| `id` | string | yes | The ID of the link to retrieve. |
| `include[]` | array<string> | no | Related resources to include in the response. |

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
| `link` | object | Shortened link details. |
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

Through the native Linkbreakers API, this operation is `GET /v1/links/:id` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-details.md) for the provider-specific parameters and requirements.

