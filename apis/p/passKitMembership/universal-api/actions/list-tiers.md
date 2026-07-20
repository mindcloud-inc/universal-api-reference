# PassKit Membership: List Tiers

Retrieves membership tiers from a PassKit Membership program.

```
GET https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-tiers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Membership `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-tiers?connectionId=$CONNECTION_ID&limit=25&offset=0&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-tiers?${params}`, {
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
| `programId` | string | yes | PassKit Program ID used to filter tiers for a membership program. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "id": "string",
      "name": "Ava Chen",
      "passTemplateId": "string",
      "pointsOverdrawn": true,
      "programId": "string",
      "secondaryPointsOverdrawn": true,
      "shortCode": "string",
      "tierIndex": 1,
      "timezone": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | Tier creation timestamp. |
| `id` | string | PassKit membership tier identifier. |
| `name` | string | Tier name. |
| `passTemplateId` | string | Pass template identifier used for this tier. |
| `pointsOverdrawn` | boolean | Whether points overdraft is allowed. |
| `programId` | string | Parent membership program identifier. |
| `secondaryPointsOverdrawn` | boolean | Whether secondary points overdraft is allowed. |
| `shortCode` | string | Short code for the tier. |
| `tierIndex` | number | Numeric ordering/index for the tier within the program. |
| `timezone` | string | Tier timezone. |
| `updated` | string | Tier update timestamp. |

## Native endpoint

Through the native PassKit Membership API, this operation is `POST /members/tiers/list` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tiers.md) for the provider-specific parameters and requirements.

