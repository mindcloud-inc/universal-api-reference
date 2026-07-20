# Raisely: List Campaigns

Retrieves campaigns from Raisely.

```
GET https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaigns?${params}`, {
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
| `private` | boolean | no | Returns the full record when authenticated |
| `q` | string | no | Search query to find records matching |
| `path` | string | no | Filter Campaign based on their path value |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | string | no | Filter Campaign based on their mode value |
| `status` | string | no | Filter Campaign based on their status value |
| `pruneConfig` | boolean | no | In private queries, removes the campaign.config to reduce request size |
| `includeTags` | boolean | no | Also include any tags on this collection (if applicable) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowExperiments": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "feeTotal": 1,
      "goal": 1,
      "grandTotal": 1,
      "mode": "string",
      "name": "Ava Chen",
      "nonSelfDonationTotal": 1,
      "organisationUuid": "string",
      "path": "string",
      "primaryDomain": "string",
      "profile": {
        "currency": "string",
        "goal": 1,
        "name": "Ava Chen",
        "path": "string",
        "status": "string",
        "total": 1,
        "totalPercent": 1,
        "type": "string",
        "uuid": "string"
      },
      "publicKey": "string",
      "status": "string",
      "theme": "string",
      "total": 1,
      "totalPercent": 1,
      "url": "https://example.com",
      "uuid": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowExperiments` | boolean |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `feeTotal` | number |  |
| `goal` | number |  |
| `grandTotal` | number |  |
| `mode` | string |  |
| `name` | string |  |
| `nonSelfDonationTotal` | number |  |
| `organisationUuid` | string |  |
| `path` | string |  |
| `primaryDomain` | string |  |
| `profile` | object |  |
| `profile.currency` | string |  |
| `profile.goal` | number |  |
| `profile.name` | string |  |
| `profile.path` | string |  |
| `profile.status` | string |  |
| `profile.total` | number |  |
| `profile.totalPercent` | number |  |
| `profile.type` | string |  |
| `profile.uuid` | string |  |
| `publicKey` | string |  |
| `status` | string |  |
| `theme` | string |  |
| `total` | number |  |
| `totalPercent` | number |  |
| `url` | string |  |
| `uuid` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `GET /campaigns` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

