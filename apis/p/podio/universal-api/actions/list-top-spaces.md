# Podio: List Top Spaces

Retrieves top spaces from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-top-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-top-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-top-spaces?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | The max number of spaces to be returned. Example: `6`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemAccountingInfo": {},
      "name": "Ava Chen",
      "org": {},
      "orgId": 1,
      "sharefileVaultUrl": "https://example.com",
      "spaceId": 1,
      "type": "string",
      "url": "https://example.com",
      "urlLabel": "https://example.com",
      "v8EngineUpdated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemAccountingInfo` | object |  |
| `name` | string |  |
| `org` | object |  |
| `orgId` | number |  |
| `sharefileVaultUrl` | string |  |
| `spaceId` | number |  |
| `type` | string |  |
| `url` | string |  |
| `urlLabel` | string |  |
| `v8EngineUpdated` | boolean |  |

## Native endpoint

Through the native Podio API, this operation is `GET /space/top/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-spaces.md) for the provider-specific parameters and requirements.

