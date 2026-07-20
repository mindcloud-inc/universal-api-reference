# Tabidoo: Get Template

Retrieves a template from the Tabidoo marketplace.

```
GET https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tabidoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/get-template?${params}`, {
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
| `templateId` | string | yes | The Tabidoo template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "description": "string",
      "descriptionI18n": {
        "cz": "string",
        "en": "string"
      },
      "downloadCount": 1,
      "id": "string",
      "languages": [
        [
          "string"
        ]
      ],
      "name": "Ava Chen",
      "namesI18n": {
        "cz": "Ava Chen",
        "en": "Ava Chen"
      },
      "perex": "string",
      "perexI18n": {
        "cz": "string",
        "en": "string"
      },
      "pricing": {
        "model": 1,
        "priceCzk": 1,
        "priceEur": 1,
        "priceUsd": 1
      },
      "screenshots": [
        [
          {}
        ]
      ],
      "style": {
        "background": "string",
        "foreground": "string",
        "icon": "string",
        "imageUrl": "https://example.com"
      },
      "tables": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `description` | string |  |
| `descriptionI18n` | object |  |
| `descriptionI18n.cz` | string |  |
| `descriptionI18n.en` | string |  |
| `downloadCount` | number |  |
| `id` | string |  |
| `languages[]` | array<string> |  |
| `name` | string |  |
| `namesI18n` | object |  |
| `namesI18n.cz` | string |  |
| `namesI18n.en` | string |  |
| `perex` | string |  |
| `perexI18n` | object |  |
| `perexI18n.cz` | string |  |
| `perexI18n.en` | string |  |
| `pricing` | object |  |
| `pricing.model` | number |  |
| `pricing.priceCzk` | number |  |
| `pricing.priceEur` | number |  |
| `pricing.priceUsd` | number |  |
| `screenshots[]` | array<object> |  |
| `screenshots[].url` | string |  |
| `style` | object |  |
| `style.background` | string |  |
| `style.foreground` | string |  |
| `style.icon` | string |  |
| `style.imageUrl` | string |  |
| `tables[]` | array<object> |  |
| `tables[].icon` | string |  |
| `tables[].name` | string |  |
| `tables[].namesI18n` | object |  |
| `tables[].namesI18n.cz` | string |  |
| `tables[].namesI18n.en` | string |  |

## Native endpoint

Through the native Tabidoo API, this operation is `GET /templates/:templateId` (base URL `https://app.tabidoo.cloud/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

