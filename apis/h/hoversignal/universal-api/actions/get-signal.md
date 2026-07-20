# Hoversignal: Get Signal



```
GET https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/get-signal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/get-signal?connectionId=$CONNECTION_ID&signalId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signalId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/get-signal?${params}`, {
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
| `signalId` | number | yes | Signal identifier. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionText` | string | The signal action text. |
| `deviceFilter` | string | The device filter mode. |
| `discountPercent` | number | The signal discount percentage when applicable. |
| `discountTimerFormat` | string | The signal discount timer format when applicable. |
| `discountTimerMinutes` | number | The signal discount timer minutes when applicable. |
| `displayDuration` | number | How long the signal is shown. |
| `excludePages` | string | Pages excluded from the signal. |
| `frequency` | string | How often the signal is shown. |
| `iconImage` | string | The signal icon image identifier. |
| `iconType` | string | The icon used for the signal. |
| `id` | number | The signal identifier. |
| `includePages` | string | Pages included in the signal. |
| `isActive` | boolean | Whether the signal is active. |
| `isActiveCampaignEnabled` | boolean | Whether ActiveCampaign integration is enabled. |
| `isAmoCrmEnabled` | boolean | Whether AmoCRM integration is enabled. |
| `isBitrixEnabled` | boolean | Whether Bitrix integration is enabled. |
| `isGetGistEnabled` | boolean | Whether GetGist integration is enabled. |
| `isMailChimpEnabled` | boolean | Whether MailChimp integration is enabled. |
| `isRequired` | boolean | Whether the signal is required. |
| `linkUrl` | string | The signal link URL. |
| `mailChimpListId` | number | The MailChimp list identifier when configured. |
| `name` | string | The signal name. |
| `order` | number | The signal display order. |
| `pageFilterType` | string | The page filter mode. |
| `popupButtonText` | string | The popup button text. |
| `popupDescription` | string | The popup description. |
| `popupImageId` | string | The popup image identifier. |
| `popupInputPlaceholder` | string | The popup input placeholder. |
| `popupSuccessMessage` | string | The popup success message. |
| `text` | string | The signal text. |
| `type` | string | The signal type. |
| `urlMicromatch` | string | The URL micromatch filter. |
| `urlRegex` | string | The URL regex filter. |

## Native endpoint

Through the native Hoversignal API, this operation is `GET /api/v1/signals/{signalId}` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signal.md) for the provider-specific parameters and requirements.

