# RapidoForm: Create Theme

Creates a new theme in RapidoForm.

```
POST https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-theme
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidoForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-theme" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-theme', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `backgroundColor` | string | no |  |
| `bottomLineColor` | string | no |  |
| `btnBackgroundColor` | string | no |  |
| `btnTextColor` | string | no |  |
| `fontFamily` | string | no |  |
| `questionColor` | string | no |  |
| `questionTypeColor` | string | no |  |
| `textAlignment` | string | no |  |
| `themeName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundColor": "string",
      "backgroundImage": "string",
      "backgroundImageType": "string",
      "backgroundImageTypeColor": "string",
      "bgImgBrigthness": 1,
      "bottomLineColor": "string",
      "btnBackgroundColor": "string",
      "btnTextColor": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fontFamily": "string",
      "fontSize": "string",
      "fontUrl": "https://example.com",
      "Id": "string",
      "isGalleryTheme": true,
      "isPaidTheme": true,
      "logo": "string",
      "logoAltText": "string",
      "logoSize": 1,
      "logoType": "string",
      "logoTypeColor": "string",
      "questionColor": "string",
      "questionTypeColor": "string",
      "radius": "string",
      "textAlignment": "string",
      "themeCreatorId": "string",
      "themeName": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "V": 1,
      "welcomeFontSize": "string",
      "welcomeTextAlignment": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundColor` | string |  |
| `backgroundImage` | string |  |
| `backgroundImageType` | string |  |
| `backgroundImageTypeColor` | string |  |
| `bgImgBrigthness` | number |  |
| `bottomLineColor` | string |  |
| `btnBackgroundColor` | string |  |
| `btnTextColor` | string |  |
| `createdAt` | date |  |
| `fontFamily` | string |  |
| `fontSize` | string |  |
| `fontUrl` | string |  |
| `Id` | string |  |
| `isGalleryTheme` | boolean |  |
| `isPaidTheme` | boolean |  |
| `logo` | string |  |
| `logoAltText` | string |  |
| `logoSize` | number |  |
| `logoType` | string |  |
| `logoTypeColor` | string |  |
| `questionColor` | string |  |
| `questionTypeColor` | string |  |
| `radius` | string |  |
| `textAlignment` | string |  |
| `themeCreatorId` | string |  |
| `themeName` | string |  |
| `updatedAt` | date |  |
| `V` | number |  |
| `welcomeFontSize` | string |  |
| `welcomeTextAlignment` | string |  |

## Native endpoint

Through the native RapidoForm API, this operation is `POST /api/theme` (base URL `https://www.rapidoform.com/be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-theme.md) for the provider-specific parameters and requirements.

