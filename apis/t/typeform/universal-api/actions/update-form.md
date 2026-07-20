# Typeform: Update Form



```
PUT https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Form fields definition. |
| `formId` | string | yes | Typeform form identifier. |
| `hidden` | string | no | Hidden fields configuration. |
| `logic` | string | no | Logic jumps configuration. |
| `settings` | string | no | Form settings. |
| `thankyouScreens` | string | no | Thank-you screens definition. |
| `theme` | string | no | Theme configuration. |
| `title` | string | no | Form title. |
| `type` | string | no | Form type. |
| `variables` | string | no | Form variables definition. |
| `welcomeScreens` | string | no | Welcome screens definition. |
| `workspace` | string | no | Workspace association. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "links": {
        "display": "https://example.com",
        "responses": "https://example.com"
      },
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "settings": {
        "autosaveProgress": true,
        "hideNavigation": true,
        "isPublic": true,
        "language": "string",
        "meta": {
          "allowIndexing": true
        },
        "progressBar": "string",
        "showProgressBar": true,
        "showQuestionNumber": true,
        "showTypeformBranding": true
      },
      "thankyouScreens": [
        {
          "id": "string",
          "properties": {
            "buttonText": "string",
            "showButton": true
          },
          "title": "string",
          "type": "string"
        }
      ],
      "theme": {
        "href": "string"
      },
      "title": "string",
      "type": "string",
      "workspace": {
        "href": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `id` | string | Form ID. |
| `lastUpdatedAt` | date | Last update timestamp. |
| `links` | object | Useful form links. |
| `links.display` | string | Public form URL. |
| `links.responses` | string | Responses URL. |
| `publishedAt` | date | Publish timestamp. |
| `settings` | object | Form settings. |
| `settings.autosaveProgress` | boolean | Whether progress autosave is enabled. |
| `settings.hideNavigation` | boolean | Whether navigation is hidden. |
| `settings.isPublic` | boolean | Whether form is public. |
| `settings.language` | string | Form language. |
| `settings.meta.allowIndexing` | boolean | Whether indexing is allowed. |
| `settings.progressBar` | string | Progress bar style. |
| `settings.showProgressBar` | boolean | Whether progress bar is shown. |
| `settings.showQuestionNumber` | boolean | Whether question numbers are shown. |
| `settings.showTypeformBranding` | boolean | Whether Typeform branding is shown. |
| `thankyouScreens` | array<object> | Thank-you screens. |
| `thankyouScreens[].id` | string | Thank-you screen ID. |
| `thankyouScreens[].properties` | object | Thank-you screen properties. |
| `thankyouScreens[].properties.buttonText` | string | Button text. |
| `thankyouScreens[].properties.showButton` | boolean | Whether button is shown. |
| `thankyouScreens[].title` | string | Thank-you screen title. |
| `thankyouScreens[].type` | string | Thank-you screen type. |
| `theme` | object | Theme reference. |
| `theme.href` | string | Theme URL. |
| `title` | string | Form title. |
| `type` | string | Form type. |
| `workspace` | object | Workspace reference. |
| `workspace.href` | string | Workspace URL. |

## Native endpoint

Through the native Typeform API, this operation is `PUT /forms/:formId` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form.md) for the provider-specific parameters and requirements.

