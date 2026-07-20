# Podio: List Apps by Space

Retrieves apps in a Podio space.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-apps-by-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-apps-by-space?connectionId=$CONNECTION_ID&spaceId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-apps-by-space?${params}`, {
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
| `spaceId` | number | yes | The space ID. Example: `123456`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeInactive` | boolean | no | True if inactive apps should be included. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": 1,
      "config": {},
      "currentRevision": 1,
      "defaultViewId": 1,
      "isDefault": true,
      "itemAccountingInfo": {},
      "link": "https://example.com",
      "linkAdd": "https://example.com",
      "original": 1,
      "sharefileVaultUrl": "https://example.com",
      "spaceId": 1,
      "status": "string",
      "url": "https://example.com",
      "urlAdd": "https://example.com",
      "urlLabel": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | number |  |
| `config` | object |  |
| `currentRevision` | number |  |
| `defaultViewId` | number |  |
| `isDefault` | boolean |  |
| `itemAccountingInfo` | object |  |
| `link` | string |  |
| `linkAdd` | string |  |
| `original` | number |  |
| `sharefileVaultUrl` | string |  |
| `spaceId` | number |  |
| `status` | string |  |
| `url` | string |  |
| `urlAdd` | string |  |
| `urlLabel` | string |  |

## Native endpoint

Through the native Podio API, this operation is `GET /app/space/:space_id/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apps-by-space.md) for the provider-specific parameters and requirements.

