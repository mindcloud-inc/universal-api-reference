# Hoversignal: Update Signal



```
PUT https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/update-signal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/update-signal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signalId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/update-signal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signalId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `signalId` | number | yes | Signal identifier. Default: `1`. |
| `type` | string | no |  |
| `iconType` | string | no |  |
| `order` | number | no |  |
| `displayDuration` | number | no |  |
| `frequency` | string | no |  |
| `pageFilterType` | string | no |  |
| `deviceFilter` | string | no |  |
| `isActive` | boolean | no |  |
| `isRequired` | boolean | no |  |
| `text` | string | no |  |
| `actionText` | string | no |  |
| `linkUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "signal": {
        "actionText": "string",
        "deviceFilter": "string",
        "discountPercent": 1,
        "discountTimerFormat": "string",
        "discountTimerMinutes": 1,
        "displayDuration": 1,
        "excludePages": "string",
        "frequency": "string",
        "iconImage": "string",
        "iconType": "string",
        "id": 1,
        "includePages": "string",
        "isActive": true,
        "isActiveCampaignEnabled": true,
        "isAmoCrmEnabled": true,
        "isBitrixEnabled": true,
        "isGetGistEnabled": true,
        "isMailChimpEnabled": true,
        "isRequired": true,
        "linkUrl": "https://example.com",
        "mailChimpListId": 1,
        "name": "Ava Chen",
        "order": 1,
        "pageFilterType": "string",
        "popupButtonText": "string",
        "popupDescription": "string",
        "popupImageId": "string",
        "popupInputPlaceholder": "string",
        "popupSuccessMessage": "string",
        "text": "string",
        "type": "string",
        "urlMicromatch": "https://example.com",
        "urlRegex": "https://example.com"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `signal` | object | The updated signal. |
| `signal.actionText` | string | The signal action text. |
| `signal.deviceFilter` | string | The device filter mode. |
| `signal.discountPercent` | number | The signal discount percentage when applicable. |
| `signal.discountTimerFormat` | string | The signal discount timer format when applicable. |
| `signal.discountTimerMinutes` | number | The signal discount timer minutes when applicable. |
| `signal.displayDuration` | number | How long the signal is shown. |
| `signal.excludePages` | string | Pages excluded from the signal. |
| `signal.frequency` | string | How often the signal is shown. |
| `signal.iconImage` | string | The signal icon image identifier. |
| `signal.iconType` | string | The icon used for the signal. |
| `signal.id` | number | The signal identifier. |
| `signal.includePages` | string | Pages included in the signal. |
| `signal.isActive` | boolean | Whether the signal is active. |
| `signal.isActiveCampaignEnabled` | boolean | Whether ActiveCampaign integration is enabled. |
| `signal.isAmoCrmEnabled` | boolean | Whether AmoCRM integration is enabled. |
| `signal.isBitrixEnabled` | boolean | Whether Bitrix integration is enabled. |
| `signal.isGetGistEnabled` | boolean | Whether GetGist integration is enabled. |
| `signal.isMailChimpEnabled` | boolean | Whether MailChimp integration is enabled. |
| `signal.isRequired` | boolean | Whether the signal is required. |
| `signal.linkUrl` | string | The signal link URL. |
| `signal.mailChimpListId` | number | The MailChimp list identifier when configured. |
| `signal.name` | string | The signal name. |
| `signal.order` | number | The signal display order. |
| `signal.pageFilterType` | string | The page filter mode. |
| `signal.popupButtonText` | string | The popup button text. |
| `signal.popupDescription` | string | The popup description. |
| `signal.popupImageId` | string | The popup image identifier. |
| `signal.popupInputPlaceholder` | string | The popup input placeholder. |
| `signal.popupSuccessMessage` | string | The popup success message. |
| `signal.text` | string | The signal text. |
| `signal.type` | string | The signal type. |
| `signal.urlMicromatch` | string | The URL micromatch filter. |
| `signal.urlRegex` | string | The URL regex filter. |
| `success` | boolean | Whether the signal was updated successfully. |

## Native endpoint

Through the native Hoversignal API, this operation is `PATCH /api/v1/signals/{signalId}` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-signal.md) for the provider-specific parameters and requirements.

