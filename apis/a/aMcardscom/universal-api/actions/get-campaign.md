# AMcards.com: Get Campaign

Retrieves a specific campaign from AMcards.com.

```
GET https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AMcards.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-campaign?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | number | no | AMcards campaign identifier from the `/campaign/` resource URI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignCost": 1,
      "dripCount": 1,
      "hasAnniversaryDrip": true,
      "hasBirthdayDrip": true,
      "id": 1,
      "isCampaignWizardCampaign": true,
      "owner": "string",
      "resourceUri": "string",
      "sendEvenIfDuplicate": true,
      "title": "string",
      "uniqueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignCost` | number |  |
| `dripCount` | number |  |
| `hasAnniversaryDrip` | boolean |  |
| `hasBirthdayDrip` | boolean |  |
| `id` | number |  |
| `isCampaignWizardCampaign` | boolean |  |
| `owner` | string |  |
| `resourceUri` | string |  |
| `sendEvenIfDuplicate` | boolean |  |
| `title` | string |  |
| `uniqueId` | string |  |

## Native endpoint

Through the native AMcards.com API, this operation is `GET /campaign/:campaignId/` (base URL `https://amcards.com/.api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

