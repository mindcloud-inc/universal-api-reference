# Typeform: Retrieve Theme



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-theme
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-theme?connectionId=$CONNECTION_ID&themeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "themeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-theme?${params}`, {
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
| `themeId` | string | yes | Typeform theme identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": {
        "brightness": 1,
        "href": "string",
        "layout": "string"
      },
      "colors": {
        "answer": "string",
        "background": "string",
        "button": "string",
        "question": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": {
        "alignment": "string",
        "fontSize": "string"
      },
      "font": "string",
      "hasTransparentButton": true,
      "id": "string",
      "name": "Ava Chen",
      "roundedCorners": "string",
      "screens": {
        "alignment": "string",
        "fontSize": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | object | Theme background configuration. |
| `background.brightness` | number | Background brightness. |
| `background.href` | string | Background image URL. |
| `background.layout` | string | Background layout. |
| `colors` | object | Theme colors. |
| `colors.answer` | string | Answer color. |
| `colors.background` | string | Background color. |
| `colors.button` | string | Button color. |
| `colors.question` | string | Question color. |
| `createdAt` | date | Theme creation timestamp. |
| `fields` | object | Field style settings. |
| `fields.alignment` | string | Field alignment. |
| `fields.fontSize` | string | Field font size. |
| `font` | string | Theme font. |
| `hasTransparentButton` | boolean | Whether buttons are transparent. |
| `id` | string | Theme ID. |
| `name` | string | Theme name. |
| `roundedCorners` | string | Corner radius setting. |
| `screens` | object | Screen style settings. |
| `screens.alignment` | string | Screen alignment. |
| `screens.fontSize` | string | Screen font size. |
| `updatedAt` | date | Theme last update timestamp. |
| `visibility` | string | Theme visibility. |

## Native endpoint

Through the native Typeform API, this operation is `GET /themes/:themeId` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-theme.md) for the provider-specific parameters and requirements.

