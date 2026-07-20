# Tabidoo: List App Tables

Retrieves tables for an application in Tabidoo.

```
GET https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/list-app-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tabidoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/list-app-tables?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/list-app-tables?${params}`, {
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
      "header": "string",
      "id": "string",
      "internalNameApi": "Ava Chen",
      "items": [
        [
          {}
        ]
      ],
      "scripts": [
        [
          {}
        ]
      ],
      "settings": {
        "userFilters": [
          [
            {}
          ]
        ]
      },
      "shortid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `header` | string | Table header. |
| `id` | string | Table ID. |
| `internalNameApi` | string | Internal API name of the table. |
| `items[]` | array<object> | Table fields. |
| `items[].header` | string | Field header. |
| `items[].metadata` | object | Field metadata. |
| `items[].metadata.description` | string | Field description. |
| `items[].metadata.filterableFields[]` | array<string> | Filterable linked-field keys. |
| `items[].metadata.required` | boolean | Whether the field is required. |
| `items[].name` | string | Field name. |
| `items[].type` | string | Field data type. |
| `scripts[]` | array<object> | Table form scripts. |
| `scripts[].name` | string | Script name. |
| `scripts[].script` | string | Script body. |
| `settings` | object | Table settings. |
| `settings.userFilters[]` | array<object> | Predefined user filters. |
| `shortid` | string | Table short ID. |

## Native endpoint

Through the native Tabidoo API, this operation is `GET /apps/:appId/tables` (base URL `https://app.tabidoo.cloud/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-app-tables.md) for the provider-specific parameters and requirements.

