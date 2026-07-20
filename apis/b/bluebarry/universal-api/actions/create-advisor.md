# Bluebarry: Create Advisor

Creates a new advisor in Bluebarry.

```
POST https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-advisor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-advisor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-advisor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native Bluebarry API, this operation is `POST /data/Advisors` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-advisor.md) for the provider-specific parameters and requirements.

