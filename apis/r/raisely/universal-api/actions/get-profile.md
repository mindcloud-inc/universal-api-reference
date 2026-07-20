# Raisely: Get Profile

Retrieves a profile from Raisely.

```
GET https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-profile?connectionId=$CONNECTION_ID&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-profile?${params}`, {
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
| `path` | string | yes | The `uuid` or `path` of the record |
| `campaign` | string | no | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | boolean | no | Returns the full record when authenticated |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityTotal": 1,
      "authorisations": [
        "string"
      ],
      "badges": [
        "string"
      ],
      "campaignTotal": 1,
      "campaignUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "exerciseTotal": 1,
      "exerciseTotalTime": 1,
      "feeTotal": 1,
      "goal": 1,
      "grandTotal": 1,
      "memberCount": 1,
      "name": "Ava Chen",
      "nonSelfDonationTotal": 1,
      "paid": true,
      "path": "string",
      "photoUrl": "https://example.com",
      "selfDonationTotal": 1,
      "status": "string",
      "tags": [
        "string"
      ],
      "total": 1,
      "totalPercent": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "firstName": "Ava",
        "permission": "string",
        "photoUrl": "https://example.com",
        "preferredName": "Ava Chen",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityTotal` | number |  |
| `authorisations` | array<string> |  |
| `badges` | array<string> |  |
| `campaignTotal` | number |  |
| `campaignUuid` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `description` | string |  |
| `exerciseTotal` | number |  |
| `exerciseTotalTime` | number |  |
| `feeTotal` | number |  |
| `goal` | number |  |
| `grandTotal` | number |  |
| `memberCount` | number |  |
| `name` | string |  |
| `nonSelfDonationTotal` | number |  |
| `paid` | boolean |  |
| `path` | string |  |
| `photoUrl` | string |  |
| `selfDonationTotal` | number |  |
| `status` | string |  |
| `tags` | array<string> |  |
| `total` | number |  |
| `totalPercent` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `user.createdAt` | date |  |
| `user.firstName` | string |  |
| `user.permission` | string |  |
| `user.photoUrl` | string |  |
| `user.preferredName` | string |  |
| `user.status` | string |  |
| `user.updatedAt` | date |  |
| `user.uuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `GET /profiles/:path` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

