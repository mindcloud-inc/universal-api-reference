# pretix: Get Organizer Settings

Retrieves organizer settings from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-organizer-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-organizer-settings?connectionId=$CONNECTION_ID&organizer=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-organizer-settings?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessibilityTitle": {
        "en": "string"
      },
      "cookieConsent": true,
      "cookieConsentDialogButtonNo": {
        "en": "string"
      },
      "cookieConsentDialogButtonYes": {
        "en": "string"
      },
      "cookieConsentDialogText": {
        "en": "string"
      },
      "cookieConsentDialogTextSecondary": {
        "en": "string"
      },
      "cookieConsentDialogTitle": {
        "en": "string"
      },
      "customerAccounts": true,
      "customerAccountsLinkByEmail": true,
      "customerAccountsNative": true,
      "customerAccountsRequireLoginForOrderAccess": true,
      "eventListAvailability": true,
      "eventListType": "string",
      "eventTeamProvisioning": true,
      "giftcardLength": 1,
      "invoiceRegenerateAllowed": true,
      "locales": [
        "string"
      ],
      "organizerHomepageText": {
        "en": "string"
      },
      "organizerInfoText": {
        "en": "string"
      },
      "organizerLinkBack": true,
      "organizerLogoImageInherit": true,
      "organizerLogoImageLarge": true,
      "primaryColor": "string",
      "primaryFont": "string",
      "region": "string",
      "reusableMediaActive": true,
      "reusableMediaTypeBarcode": true,
      "reusableMediaTypeBarcodeIdentifierLength": 1,
      "reusableMediaTypeNfcMf0aes": true,
      "reusableMediaTypeNfcMf0aesAutocreateGiftcard": true,
      "reusableMediaTypeNfcMf0aesAutocreateGiftcardCurrency": "string",
      "reusableMediaTypeNfcMf0aesRandomUid": true,
      "reusableMediaTypeNfcUid": true,
      "reusableMediaTypeNfcUidAutocreateGiftcard": true,
      "reusableMediaTypeNfcUidAutocreateGiftcardCurrency": "string",
      "themeColorBackground": "string",
      "themeColorDanger": "string",
      "themeColorSuccess": "string",
      "themeRoundBorders": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibilityTitle.en` | string |  |
| `cookieConsent` | boolean |  |
| `cookieConsentDialogButtonNo.en` | string |  |
| `cookieConsentDialogButtonYes.en` | string |  |
| `cookieConsentDialogText.en` | string |  |
| `cookieConsentDialogTextSecondary.en` | string |  |
| `cookieConsentDialogTitle.en` | string |  |
| `customerAccounts` | boolean |  |
| `customerAccountsLinkByEmail` | boolean |  |
| `customerAccountsNative` | boolean |  |
| `customerAccountsRequireLoginForOrderAccess` | boolean |  |
| `eventListAvailability` | boolean |  |
| `eventListType` | string |  |
| `eventTeamProvisioning` | boolean |  |
| `giftcardLength` | number |  |
| `invoiceRegenerateAllowed` | boolean |  |
| `locales[]` | string |  |
| `organizerHomepageText.en` | string |  |
| `organizerInfoText.en` | string |  |
| `organizerLinkBack` | boolean |  |
| `organizerLogoImageInherit` | boolean |  |
| `organizerLogoImageLarge` | boolean |  |
| `primaryColor` | string |  |
| `primaryFont` | string |  |
| `region` | string |  |
| `reusableMediaActive` | boolean |  |
| `reusableMediaTypeBarcode` | boolean |  |
| `reusableMediaTypeBarcodeIdentifierLength` | number |  |
| `reusableMediaTypeNfcMf0aes` | boolean |  |
| `reusableMediaTypeNfcMf0aesAutocreateGiftcard` | boolean |  |
| `reusableMediaTypeNfcMf0aesAutocreateGiftcardCurrency` | string |  |
| `reusableMediaTypeNfcMf0aesRandomUid` | boolean |  |
| `reusableMediaTypeNfcUid` | boolean |  |
| `reusableMediaTypeNfcUidAutocreateGiftcard` | boolean |  |
| `reusableMediaTypeNfcUidAutocreateGiftcardCurrency` | string |  |
| `themeColorBackground` | string |  |
| `themeColorDanger` | string |  |
| `themeColorSuccess` | string |  |
| `themeRoundBorders` | boolean |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/settings/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organizer-settings.md) for the provider-specific parameters and requirements.

