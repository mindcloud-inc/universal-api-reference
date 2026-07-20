# ReplyCX: List Bots



```
GET https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/list-bots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReplyCX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/list-bots?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "botLeadId": 1,
      "botOwnerId": 1,
      "botOwnerName": "Ava Chen",
      "botTitle": "string",
      "campaignDetails": {},
      "categoryName": {},
      "channels": [
        {
          "configurationId": 1,
          "name": "Ava Chen"
        }
      ],
      "createdAt": "string",
      "designTool": "string",
      "isActive": true,
      "isInactiveBySystem": true,
      "isPreferredBot": true,
      "isVisible": 1,
      "lastDeployedAt": "string",
      "outboundType": {},
      "preferredBotLanguage": {
        "code": "string",
        "label": "string"
      },
      "previewKey": "string",
      "priority": 1,
      "publishKey": "string",
      "role": {
        "id": 1,
        "role": "string"
      },
      "spreadsheetLink": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botLeadId` | number |  |
| `botOwnerId` | number |  |
| `botOwnerName` | string |  |
| `botTitle` | string |  |
| `campaignDetails` | object |  |
| `categoryName` | object |  |
| `channels[].configurationId` | number |  |
| `channels[].name` | string |  |
| `createdAt` | string |  |
| `designTool` | string |  |
| `isActive` | boolean |  |
| `isInactiveBySystem` | boolean |  |
| `isPreferredBot` | boolean |  |
| `isVisible` | number |  |
| `lastDeployedAt` | string |  |
| `outboundType` | object |  |
| `preferredBotLanguage.code` | string |  |
| `preferredBotLanguage.label` | string |  |
| `previewKey` | string |  |
| `priority` | number |  |
| `publishKey` | string |  |
| `role.id` | number |  |
| `role.role` | string |  |
| `spreadsheetLink` | object |  |
| `type` | string |  |

## Native endpoint

Through the native ReplyCX API, this operation is `GET /v1/accounts/:account_id/bots` (base URL `https://api.reply.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bots.md) for the provider-specific parameters and requirements.

