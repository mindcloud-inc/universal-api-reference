# Typeform: Auto-Translate Form



```
POST https://connect.mindcloud.co/v1/universal/typeform/latest/actions/auto-translate-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/auto-translate-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "language": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/auto-translate-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "language": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Typeform form identifier. |
| `language` | string | yes | Language code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {
          "attachment": {
            "properties": {
              "description": "string"
            }
          },
          "id": "string",
          "layout": {
            "attachment": {
              "properties": {
                "description": "string"
              }
            }
          },
          "properties": {
            "buttonText": "string",
            "choices": [
              {
                "attachment": {
                  "properties": {
                    "description": "string"
                  }
                },
                "id": "string",
                "label": "string"
              }
            ],
            "description": "string",
            "labels": {
              "center": "string",
              "left": "string",
              "right": "string"
            }
          },
          "title": "string"
        }
      ],
      "messages": {
        "block": {
          "dropdownPlaceholder": "string",
          "longtextHint": "string",
          "shortTextPlaceholder": "string"
        },
        "label": {
          "buttonOk": "string",
          "buttonSubmit": "string",
          "errorRequired": "string",
          "warningConnection": "string"
        }
      },
      "thankyouScreens": [
        {
          "attachment": {
            "properties": {
              "description": "string"
            }
          },
          "id": "string",
          "layout": {
            "attachment": {
              "properties": {
                "description": "string"
              }
            }
          },
          "properties": {
            "buttonText": "string",
            "description": "string"
          },
          "title": "string"
        }
      ],
      "welcomeScreens": [
        {
          "attachment": {
            "properties": {
              "description": "string"
            }
          },
          "id": "string",
          "layout": {
            "attachment": {
              "properties": {
                "description": "string"
              }
            }
          },
          "properties": {
            "buttonText": "string",
            "description": "string"
          },
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | Translated form fields. |
| `fields[].attachment` | object | Field attachment translation object. |
| `fields[].attachment.properties` | object | Field attachment properties. |
| `fields[].attachment.properties.description` | string | Translated attachment description. |
| `fields[].id` | string | Translated field ID. |
| `fields[].layout` | object | Translated field layout. |
| `fields[].layout.attachment` | object | Layout attachment translation object. |
| `fields[].layout.attachment.properties` | object | Layout attachment properties. |
| `fields[].layout.attachment.properties.description` | string | Translated layout attachment description. |
| `fields[].properties` | object | Translated field properties. |
| `fields[].properties.buttonText` | string | Translated button text. |
| `fields[].properties.choices` | array<object> | Translated choice labels. |
| `fields[].properties.choices[].attachment` | object | Choice attachment translation object. |
| `fields[].properties.choices[].attachment.properties` | object | Choice attachment properties. |
| `fields[].properties.choices[].attachment.properties.description` | string | Translated choice attachment description. |
| `fields[].properties.choices[].id` | string | Choice ID. |
| `fields[].properties.choices[].label` | string | Translated choice label. |
| `fields[].properties.description` | string | Translated field description. |
| `fields[].properties.labels` | object | Translated opinion scale labels. |
| `fields[].properties.labels.center` | string | Translated center label. |
| `fields[].properties.labels.left` | string | Translated left label. |
| `fields[].properties.labels.right` | string | Translated right label. |
| `fields[].title` | string | Translated field title. |
| `messages` | object | Translated form messages. |
| `messages.block` | object | Translated block messages. |
| `messages.block.dropdownPlaceholder` | string | Translated dropdown placeholder. |
| `messages.block.longtextHint` | string | Translated long-text hint. |
| `messages.block.shortTextPlaceholder` | string | Translated short-text placeholder. |
| `messages.label` | object | Translated label messages. |
| `messages.label.buttonOk` | string | Translated ok label. |
| `messages.label.buttonSubmit` | string | Translated submit label. |
| `messages.label.errorRequired` | string | Translated required validation message. |
| `messages.label.warningConnection` | string | Translated connection warning message. |
| `thankyouScreens` | array<object> | Translated thank-you screens. |
| `thankyouScreens[].attachment` | object | Thank-you screen attachment translation object. |
| `thankyouScreens[].attachment.properties` | object | Thank-you screen attachment properties. |
| `thankyouScreens[].attachment.properties.description` | string | Translated thank-you screen attachment description. |
| `thankyouScreens[].id` | string | Thank-you screen ID. |
| `thankyouScreens[].layout` | object | Thank-you screen layout translation object. |
| `thankyouScreens[].layout.attachment` | object | Thank-you layout attachment translation object. |
| `thankyouScreens[].layout.attachment.properties` | object | Thank-you layout attachment properties. |
| `thankyouScreens[].layout.attachment.properties.description` | string | Translated thank-you layout attachment description. |
| `thankyouScreens[].properties` | object | Translated thank-you screen properties. |
| `thankyouScreens[].properties.buttonText` | string | Translated thank-you button text. |
| `thankyouScreens[].properties.description` | string | Translated thank-you description text. |
| `thankyouScreens[].title` | string | Translated thank-you screen title. |
| `welcomeScreens` | array<object> | Translated welcome screens. |
| `welcomeScreens[].attachment` | object | Welcome screen attachment translation object. |
| `welcomeScreens[].attachment.properties` | object | Welcome screen attachment properties. |
| `welcomeScreens[].attachment.properties.description` | string | Translated welcome screen attachment description. |
| `welcomeScreens[].id` | string | Welcome screen ID. |
| `welcomeScreens[].layout` | object | Welcome screen layout translation object. |
| `welcomeScreens[].layout.attachment` | object | Welcome layout attachment translation object. |
| `welcomeScreens[].layout.attachment.properties` | object | Welcome layout attachment properties. |
| `welcomeScreens[].layout.attachment.properties.description` | string | Translated welcome layout attachment description. |
| `welcomeScreens[].properties` | object | Translated welcome screen properties. |
| `welcomeScreens[].properties.buttonText` | string | Translated welcome button text. |
| `welcomeScreens[].properties.description` | string | Translated welcome description text. |
| `welcomeScreens[].title` | string | Translated welcome screen title. |

## Native endpoint

Through the native Typeform API, this operation is `POST /forms/:formId/translations/:language/auto` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auto-translate-form.md) for the provider-specific parameters and requirements.

