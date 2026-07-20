# DatoCMS: Publish Record



```
PUT https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/publish-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/publish-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "T4m4tPymSACFzsqbZS65WA"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/publish-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "T4m4tPymSACFzsqbZS65WA"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | yes | Example: `T4m4tPymSACFzsqbZS65WA`. |
| `contentInLocales` | list<string> | no | Locales to publish in selective publish mode. Example: `en`. |
| `nonLocalizedContent` | boolean | no | Whether to include non-localized content in selective publish mode. Example: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recursive` | boolean | no | Publish parent records recursively when required by tree relationships. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "meta": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `meta` | object |  |
| `relationships` | object |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `PUT /items/:itemId/publish` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-record.md) for the provider-specific parameters and requirements.

