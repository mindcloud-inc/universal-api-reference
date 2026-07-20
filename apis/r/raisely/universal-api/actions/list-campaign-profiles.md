# Raisely: List Campaign Profiles

Retrieves profiles from a Raisely campaign.

```
GET https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaign-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaign-profiles?connectionId=$CONNECTION_ID&limit=25&offset=0&campaign=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaign": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaign-profiles?${params}`, {
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
| `campaign` | string | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | boolean | no | Returns the full record when authenticated |
| `q` | string | no | Search query to find records matching |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityTotal": 1,
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
      "name": "Ava Chen",
      "nonSelfDonationTotal": 1,
      "paid": true,
      "path": "string",
      "photoUrl": "https://example.com",
      "selfDonationTotal": 1,
      "status": "string",
      "total": 1,
      "totalPercent": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
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
| `name` | string |  |
| `nonSelfDonationTotal` | number |  |
| `paid` | boolean |  |
| `path` | string |  |
| `photoUrl` | string |  |
| `selfDonationTotal` | number |  |
| `status` | string |  |
| `total` | number |  |
| `totalPercent` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `GET /campaigns/:campaign/profiles` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-profiles.md) for the provider-specific parameters and requirements.

