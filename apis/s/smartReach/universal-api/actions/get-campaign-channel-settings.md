# SmartReach: Get Campaign Channel Settings

Retrieves campaign channel settings from SmartReach.

```
GET https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-campaign-channel-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-campaign-channel-settings?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-campaign-channel-settings?${params}`, {
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
| `campaignId` | string | yes | ID of campaign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel_settings": {
        "call_settings": [
          {
            "id": "string"
          }
        ],
        "email_settings": [
          {
            "id": "ava@example.com"
          }
        ],
        "general_settings": [
          {
            "id": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel_settings.call_settings[].id` | string |  |
| `channel_settings.email_settings[].id` | string |  |
| `channel_settings.general_settings[].id` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `GET /campaigns/:campaign_id/channel_settings` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-channel-settings.md) for the provider-specific parameters and requirements.

