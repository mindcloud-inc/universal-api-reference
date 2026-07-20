# Tabidoo: Get App

Retrieves an application from a Tabidoo workspace.

```
GET https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/get-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tabidoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/get-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/get-app?${params}`, {
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
| `appId` | string | yes | The Tabidoo application ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "internalName": "Ava Chen",
      "isMultiLanguage": true,
      "modules": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "namesI18n": {
        "en": "Ava Chen"
      },
      "tables": [
        [
          "string"
        ]
      ],
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `internalName` | string |  |
| `isMultiLanguage` | boolean |  |
| `modules[]` | array<object> |  |
| `modules[].header` | string |  |
| `modules[].shortId` | string |  |
| `modules[].tableIds[]` | array<string> |  |
| `name` | string |  |
| `namesI18n` | object |  |
| `namesI18n.en` | string |  |
| `tables[]` | array |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Tabidoo API, this operation is `GET /apps/:appId` (base URL `https://app.tabidoo.cloud/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app.md) for the provider-specific parameters and requirements.

