# NetSuite - Basic: Get Record Types

Retrieves details for the record types in NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-record-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-record-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/get-record-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "__meta": {
        "presentation": {
          "entityUrl": "https://example.com",
          "fields": {
            "name": "Ava Chen"
          },
          "type": "string"
        }
      },
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "mediaType": "https://example.com",
          "rel": "https://example.com"
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__meta` | object |  |
| `__meta.presentation` | object |  |
| `__meta.presentation.entityUrl` | string |  |
| `__meta.presentation.fields` | object |  |
| `__meta.presentation.fields.name` | string |  |
| `__meta.presentation.type` | string |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].mediaType` | string |  |
| `links[].rel` | string |  |
| `name` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/metadata-catalog` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-types.md) for the provider-specific parameters and requirements.

