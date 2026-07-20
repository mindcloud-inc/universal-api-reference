# Bluebarry Universal API Examples

These examples use the MindCloud API key and Bluebarry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Advisors

Retrieves advisor entity records from Bluebarry.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-advisors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-advisors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [List Advisors action reference](actions/list-advisors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bluebarry/latest/actions/list-advisors).

## Create Advisor

Creates a new advisor in Bluebarry.

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

Example response:

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

See the full [Create Advisor action reference](actions/create-advisor.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bluebarry/latest/actions/create-advisor).
