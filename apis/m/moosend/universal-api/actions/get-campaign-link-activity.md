# Moosend: Get Campaign Link Activity

Retrieves campaign link activity from Moosend.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-link-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-link-activity?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-link-activity?${params}`, {
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
| `campaignId` | string | yes | The ID of the campaign that you want to get link activity by location of. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "contextDescription": "string",
      "contextName": "Ava Chen",
      "timestamp": "string",
      "totalCount": 1,
      "uniqueCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string |  |
| `contextDescription` | string |  |
| `contextName` | string |  |
| `timestamp` | string |  |
| `totalCount` | number |  |
| `uniqueCount` | number |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /campaigns/{{CampaignID}}/stats/links.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-link-activity.md) for the provider-specific parameters and requirements.

