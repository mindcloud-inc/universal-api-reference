# Belong: List Related Hubs

Retrieves related hubs from Belong by hub ID or slug.

```
GET https://connect.mindcloud.co/v1/universal/belong/latest/actions/list-related-hubs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Belong `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/belong/latest/actions/list-related-hubs?connectionId=$CONNECTION_ID&id=belong" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "belong"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/belong/latest/actions/list-related-hubs?${params}`, {
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
| `withMarkers` | boolean | no |  |
| `page` | number | no | Example: `1`. |
| `limit` | number | no | Example: `20`. |
| `cursor` | string | no | Example: `60a763d0b9b1c60004040404`. |

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
      "description": "string",
      "externalLink": "https://example.com",
      "gasless": true,
      "geoRestrictedMinting": true,
      "hubType": "string",
      "id": "string",
      "isJoined": true,
      "locale": "string",
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
| `description` | string | Related hub description. |
| `externalLink` | string | External link configured for the hub. |
| `gasless` | boolean | Whether gasless flows are enabled. |
| `geoRestrictedMinting` | boolean | Whether minting is geo-restricted. |
| `hubType` | string | Belong hub type. |
| `id` | string | Belong related hub ID. |
| `isJoined` | boolean | Whether the current user is joined to the related hub. |
| `locale` | string | Hub locale. |
| `location` | object | Hub geolocation object. |
| `mediaData` | object | Resolved media variants and dominant colors. |
| `membersIDs` | array<string> | Member user IDs. |
| `name` | string | Related hub display name. |
| `nftMedia` | object | NFT media metadata when present. |
| `ownerId` | string | Owner user ID. |
| `paperServiceAllowed` | boolean | Whether paper service is allowed. |
| `passStrategy` | string | Pass issuance strategy when configured. |
| `place` | object | Hub place metadata. |
| `private` | boolean | Whether the hub is private. |
| `propertyId` | string | Associated property ID when present. |
| `relatedHubIDs` | array<string> | Related hub IDs. |
| `relatedToIDs` | array<string> | Reverse-related hub IDs. |
| `slug` | string | Public hub slug. |
| `source` | string | System that created the hub. |
| `status` | string | Publication status for the related hub. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Belong API, this operation is `GET /hubs/:id/related` (base URL `https://api.belong.net/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-related-hubs.md) for the provider-specific parameters and requirements.

