# Bluebarry: Get Advisor

Retrieves a single advisor from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-advisor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-advisor?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-advisor?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "advisorResultSettings": "string",
      "advisorResultSettingsId": "string",
      "advisorStartPageSettings": "string",
      "advisorStartPageSettingsId": "string",
      "cards": [
        {}
      ],
      "clonedFrom": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "currencyIso": "string",
      "description": "string",
      "displayType": "string",
      "filters": [
        {}
      ],
      "id": "string",
      "imageUrl": "https://example.com",
      "klaviyoIntegration": "string",
      "klaviyoIntegrationId": "string",
      "links": [
        {}
      ],
      "matIcon": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifierId": "string",
      "name": "Ava Chen",
      "preResultDescription": "string",
      "preResultImageFocalPointX": "string",
      "preResultImageFocalPointY": "string",
      "preResultImageUrl": "https://example.com",
      "preResultPageDesktopLayout": "string",
      "preResultPageMobileLayout": "string",
      "preResultPageShowDescription": true,
      "preResultPageShowImage": true,
      "preResultTitle": "string",
      "productCheckEnabled": true,
      "productCheckMatchCtaText": "string",
      "productCheckMatchCurrentProductLabel": "string",
      "productCheckMatchLabelOne": "string",
      "productCheckMatchLabelTwo": "string",
      "productCheckMatchProductLabel": "string",
      "productCheckMatchTitle": "string",
      "productCheckNoMatchCtaText": "string",
      "productCheckNoMatchCurrentProductLabel": "string",
      "productCheckNoMatchLabelOne": "string",
      "productCheckNoMatchLabelTwo": "string",
      "productCheckNoMatchProductLabel": "string",
      "productCheckNoMatchTitle": "string",
      "productCheckPreResultDescription": "string",
      "productCheckPreResultImageFocalPointX": "string",
      "productCheckPreResultImageFocalPointY": "string",
      "productCheckPreResultImageUrl": "https://example.com",
      "productCheckPreResultPageDesktopLayout": "string",
      "productCheckPreResultPageMobileLayout": "string",
      "productCheckPreResultPageShowDescription": true,
      "productCheckPreResultPageShowImage": true,
      "productCheckPreResultTitle": "string",
      "productCheckThresholdPercentage": 1,
      "questions": [
        {}
      ],
      "reference": "string",
      "showPreResultPage": true,
      "showProductCheckPreResultPage": true,
      "tenant": "string",
      "tenantId": "string",
      "theme": "string",
      "themeId": "string",
      "treatVariantsAsSeparateProducts": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advisorResultSettings` | string |  |
| `advisorResultSettingsId` | string |  |
| `advisorStartPageSettings` | string |  |
| `advisorStartPageSettingsId` | string |  |
| `cards` | array<object> |  |
| `clonedFrom` | string |  |
| `createdDate` | date |  |
| `creatorId` | string |  |
| `currencyIso` | string |  |
| `description` | string |  |
| `displayType` | string |  |
| `filters` | array<object> |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `klaviyoIntegration` | string |  |
| `klaviyoIntegrationId` | string |  |
| `links` | array<object> |  |
| `matIcon` | string |  |
| `modifiedDate` | date |  |
| `modifierId` | string |  |
| `name` | string |  |
| `preResultDescription` | string |  |
| `preResultImageFocalPointX` | string |  |
| `preResultImageFocalPointY` | string |  |
| `preResultImageUrl` | string |  |
| `preResultPageDesktopLayout` | string |  |
| `preResultPageMobileLayout` | string |  |
| `preResultPageShowDescription` | boolean |  |
| `preResultPageShowImage` | boolean |  |
| `preResultTitle` | string |  |
| `productCheckEnabled` | boolean |  |
| `productCheckMatchCtaText` | string |  |
| `productCheckMatchCurrentProductLabel` | string |  |
| `productCheckMatchLabelOne` | string |  |
| `productCheckMatchLabelTwo` | string |  |
| `productCheckMatchProductLabel` | string |  |
| `productCheckMatchTitle` | string |  |
| `productCheckNoMatchCtaText` | string |  |
| `productCheckNoMatchCurrentProductLabel` | string |  |
| `productCheckNoMatchLabelOne` | string |  |
| `productCheckNoMatchLabelTwo` | string |  |
| `productCheckNoMatchProductLabel` | string |  |
| `productCheckNoMatchTitle` | string |  |
| `productCheckPreResultDescription` | string |  |
| `productCheckPreResultImageFocalPointX` | string |  |
| `productCheckPreResultImageFocalPointY` | string |  |
| `productCheckPreResultImageUrl` | string |  |
| `productCheckPreResultPageDesktopLayout` | string |  |
| `productCheckPreResultPageMobileLayout` | string |  |
| `productCheckPreResultPageShowDescription` | boolean |  |
| `productCheckPreResultPageShowImage` | boolean |  |
| `productCheckPreResultTitle` | string |  |
| `productCheckThresholdPercentage` | number |  |
| `questions` | array<object> |  |
| `reference` | string |  |
| `showPreResultPage` | boolean |  |
| `showProductCheckPreResultPage` | boolean |  |
| `tenant` | string |  |
| `tenantId` | string |  |
| `theme` | string |  |
| `themeId` | string |  |
| `treatVariantsAsSeparateProducts` | boolean |  |

## Native endpoint

Through the native Bluebarry API, this operation is `GET /data/Advisors({id})` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-advisor.md) for the provider-specific parameters and requirements.

