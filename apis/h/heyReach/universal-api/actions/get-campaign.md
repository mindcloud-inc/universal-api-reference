# Hey Reach: Get Campaign

Retrieves a campaign from Hey Reach.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignAccountIds": [
        1
      ],
      "creationTime": "string",
      "excludeContactedFromSenderInOtherCampaign": true,
      "excludeHasOtherAccConversations": true,
      "excludeInOtherCampaigns": true,
      "excludeListId": "string",
      "id": 1,
      "linkedInUserListId": 1,
      "linkedInUserListName": "https://example.com",
      "name": "Ava Chen",
      "organizationUnitId": 1,
      "progressStats": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignAccountIds` | array<number> |  |
| `creationTime` | string |  |
| `excludeContactedFromSenderInOtherCampaign` | boolean |  |
| `excludeHasOtherAccConversations` | boolean |  |
| `excludeInOtherCampaigns` | boolean |  |
| `excludeListId` | string |  |
| `id` | number |  |
| `linkedInUserListId` | number |  |
| `linkedInUserListName` | string |  |
| `name` | string |  |
| `organizationUnitId` | number |  |
| `progressStats` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Hey Reach API, this operation is `GET /api/public/campaign/GetById` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

