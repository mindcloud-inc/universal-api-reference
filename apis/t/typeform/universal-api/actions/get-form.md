# Typeform: Get Form



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-form?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-form?${params}`, {
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
| `formId` | list | yes | Typeform form ID. |

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

Through the native Typeform API, this operation is `GET /forms/:formId` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

