# Wufoo: List Report Widgets

Retrieves widgets from a specific Wufoo report.

```
GET https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-report-widgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wufoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-report-widgets?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-report-widgets?${params}`, {
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
| `identifier` | string | yes | The report hash or identifier whose widgets to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hash": "string",
      "name": "Ava Chen",
      "size": "string",
      "type": "string",
      "typeDesc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hash` | string | The widget identifier. |
| `name` | string | The widget name. |
| `size` | string | The widget size. |
| `type` | string | The widget type. |
| `typeDesc` | string | The widget type description. |

## Native endpoint

Through the native Wufoo API, this operation is `GET /reports/:identifier/widgets.json` (base URL `https://{{credentials.subdomain}}.wufoo.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-report-widgets.md) for the provider-specific parameters and requirements.

