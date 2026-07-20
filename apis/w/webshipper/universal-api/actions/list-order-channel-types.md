# Webshipper: List Order Channel Types

Retrieves order channel types from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channel-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channel-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channel-types?${params}`, {
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
| `filter.id` | string | no | Filter by id. |
| `filter.byName` | string | no | Filter by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "canAutofulfill": true,
        "canLimitDropPoints": true,
        "description": "string",
        "hide": true,
        "listLogo": "string",
        "moduleLink": "https://example.com",
        "name": "Ava Chen",
        "supportsIdImport": true,
        "supportsRateQuoting": true,
        "supportsStatusesImport": true,
        "supportsTimeIntervalImport": true,
        "supportsVatInCheckout": true,
        "supportUrl": "https://example.com",
        "usesScheduledImport": true
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "copyright": "string"
      },
      "relationships": {
        "localAttrs": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.canAutofulfill` | boolean |  |
| `attributes.canLimitDropPoints` | boolean |  |
| `attributes.description` | string |  |
| `attributes.hide` | boolean |  |
| `attributes.listLogo` | string |  |
| `attributes.moduleLink` | string |  |
| `attributes.name` | string |  |
| `attributes.supportsIdImport` | boolean |  |
| `attributes.supportsRateQuoting` | boolean |  |
| `attributes.supportsStatusesImport` | boolean |  |
| `attributes.supportsTimeIntervalImport` | boolean |  |
| `attributes.supportsVatInCheckout` | boolean |  |
| `attributes.supportUrl` | string |  |
| `attributes.usesScheduledImport` | boolean |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `relationships.localAttrs.links.related` | string |  |
| `relationships.localAttrs.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /order_channel_types` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-channel-types.md) for the provider-specific parameters and requirements.

