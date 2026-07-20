# Charidy: List Campaign Teams

Retrieves teams for a campaign from Charidy.

```
GET https://connect.mindcloud.co/v1/universal/charidy/latest/actions/list-campaign-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charidy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charidy/latest/actions/list-campaign-teams?connectionId=$CONNECTION_ID&campaignId=4947" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "4947"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charidy/latest/actions/list-campaign-teams?${params}`, {
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
| `campaignId` | number | yes | The campaign ID whose teams to list. Example: `4947`. |
| `grouped` | boolean | no | Whether to return grouped teams. Example: `1`. |
| `offset` | number | no | Return teams starting after this offset. Example: `1`. |
| `limit` | number | no | Maximum number of teams to return. Example: `50`. |
| `sort` | string | no | Sort teams by the requested field and direction. Example: `-amount`. |
| `parentTeamId` | number | no | Filter results by parent team ID when applicable. Example: `123`. |
| `parentOnly` | boolean | no | Whether to return only parent teams. Example: `0`. |
| `grandparentOnly` | boolean | no | Whether to return only grandparent teams. Example: `0`. |
| `skipParent` | boolean | no | Whether to exclude parent teams from the results. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "campaignId": 1,
        "childTeamsCount": 1,
        "donated": 1,
        "donationN": 1,
        "hidden": true,
        "image": "string",
        "isParent": true,
        "name": "Ava Chen",
        "parentTeamId": 1,
        "shortlink": "https://example.com",
        "slug": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.campaignId` | number | Campaign ID. |
| `attributes.childTeamsCount` | number | Child team count. |
| `attributes.donated` | number | Amount donated to the team. |
| `attributes.donationN` | number | Donation count. |
| `attributes.hidden` | boolean | Whether the team is hidden. |
| `attributes.image` | string | Team image URL. |
| `attributes.isParent` | boolean | Whether the team is a parent team. |
| `attributes.name` | string | Team name. |
| `attributes.parentTeamId` | number | Parent team ID. |
| `attributes.shortlink` | string | Team short link. |
| `attributes.slug` | string | Team slug. |
| `id` | string | Unique team ID. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Charidy API, this operation is `GET /api/v1/campaign/:campaignId/teams` (base URL `https://api.charidy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-teams.md) for the provider-specific parameters and requirements.

