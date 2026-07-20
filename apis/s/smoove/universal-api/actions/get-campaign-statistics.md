# Smoove: Get Campaign Statistics

Retrieves aggregated statistics for a Smoove email campaign.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-campaign-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-campaign-statistics?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-campaign-statistics?${params}`, {
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
| `id` | string | yes |  |
| `by` | list | no | One of: `CampaignId`, `ExternalId`. Default: `CampaignId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abused": 1,
      "bounced": 1,
      "clicked": 1,
      "howManyWasBouncedHard": 1,
      "howManyWasBouncedSoft": 1,
      "howManyWasSent": 1,
      "howManyWasWatched": 1,
      "linksClicked": 1,
      "resubcribed": 1,
      "sentDate": "2026-05-07T12:00:00.000Z",
      "unsubcribed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abused` | number |  |
| `bounced` | number |  |
| `clicked` | number |  |
| `howManyWasBouncedHard` | number |  |
| `howManyWasBouncedSoft` | number |  |
| `howManyWasSent` | number |  |
| `howManyWasWatched` | number |  |
| `linksClicked` | number |  |
| `resubcribed` | number |  |
| `sentDate` | date |  |
| `unsubcribed` | number |  |

## Native endpoint

Through the native Smoove API, this operation is `GET /v1/Campaigns/:id/Statistics` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-statistics.md) for the provider-specific parameters and requirements.

