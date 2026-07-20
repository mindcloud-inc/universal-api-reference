# Affinda: Get specific data source

Retrieves a specific mapping data source from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-data-source?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-data-source?${params}`, {
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
| `identifier` | string | yes | Data source's identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayProperty": "string",
      "identifier": "string",
      "keyProperty": "string",
      "name": "Ava Chen",
      "organization": "string",
      "schema": {},
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayProperty` | string |  |
| `identifier` | string |  |
| `keyProperty` | string |  |
| `name` | string |  |
| `organization` | string |  |
| `schema` | object |  |
| `workspace` | string |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/mapping_data_sources/:identifier` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-source.md) for the provider-specific parameters and requirements.

