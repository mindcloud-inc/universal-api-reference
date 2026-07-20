# Belong: Get Hub

Retrieves a hub from Belong by ID or slug.

```
GET https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-hub
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Belong `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-hub?connectionId=$CONNECTION_ID&id=belong" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "belong"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-hub?${params}`, {
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
| `id` | string | yes | Example: `belong`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminsIDs": [
        "string"
      ],
      "allowMultiPass": true,
      "avatar": "string",
      "contracts": [
        "string"
      ],
      "countMembers": 1,
      "coverImage": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "description": "string",
      "externalLink": "https://example.com",
      "gasless": true,
      "geoRestrictedMinting": true,
      "hubType": "string",
      "id": "string",
      "linkInstagram": "https://example.com",
      "linkTwitter": "https://example.com",
      "linkWebsite": "https://example.com",
      "locale": "string",
      "localizations": [
        {}
      ],
      "location": {},
      "mediaData": {},
      "membersIDs": [
        "string"
      ],
      "name": "Ava Chen",
      "nftMedia": {},
      "ownerId": "string",
      "paperServiceAllowed": true,
      "passStrategy": "string",
      "place": {},
      "private": true,
      "propertyId": "string",
      "relatedHubIDs": [
        "string"
      ],
      "relatedToIDs": [
        "string"
      ],
      "slug": "string",
      "source": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminsIDs` | array<string> | Admin user IDs. |
| `allowMultiPass` | boolean | Whether multiple passes are allowed. |
| `avatar` | string | Avatar asset reference. |
| `contracts` | array<string> | Associated contract identifiers. |
| `countMembers` | number | Current member count. |
| `coverImage` | string | Cover image asset reference. |
| `createdAt` | date | Creation timestamp. |
| `customFields` | object |  |
| `description` | string | Hub description. |
| `externalLink` | string | External link configured for the hub. |
| `gasless` | boolean | Whether gasless flows are enabled. |
| `geoRestrictedMinting` | boolean | Whether minting is geo-restricted. |
| `hubType` | string | Belong hub type. |
| `id` | string | Belong hub ID. |
| `linkInstagram` | string |  |
| `linkTwitter` | string |  |
| `linkWebsite` | string |  |
| `locale` | string | Hub locale. |
| `localizations[]` | object |  |
| `location` | object | Hub geolocation object. |
| `mediaData` | object | Resolved media variants and dominant colors. |
| `membersIDs` | array<string> | Member user IDs. |
| `name` | string | Hub display name. |
| `nftMedia` | object | NFT media metadata when present. |
| `ownerId` | string | Owner user ID. |
| `paperServiceAllowed` | boolean | Whether paper service is allowed. |
| `passStrategy` | string | Pass issuance strategy when configured. |
| `place` | object | Hub place metadata. |
| `private` | boolean | Whether the hub is private. |
| `propertyId` | string | Associated property ID when present. |
| `relatedHubIDs` | array<string> | Related hub IDs. |
| `relatedToIDs` | array<string> | Reverse-related hub IDs. |
| `slug` | string | Hub slug. |
| `source` | string | System that created the hub. |
| `status` | string | Publication status for the hub. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Belong API, this operation is `GET /hubs/:id` (base URL `https://api.belong.net/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hub.md) for the provider-specific parameters and requirements.

