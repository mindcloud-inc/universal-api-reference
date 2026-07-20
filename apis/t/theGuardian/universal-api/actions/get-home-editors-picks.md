# The Guardian: Get Home Editors Picks

Retrieves home-page editors' picks from The Guardian.

```
GET https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-home-editors-picks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Guardian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-home-editors-picks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-home-editors-picks?${params}`, {
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
      "apiUrl": "https://example.com",
      "fields": {
        "headline": "string",
        "trailText": "string"
      },
      "id": "string",
      "isHosted": true,
      "pillarId": "string",
      "pillarName": "Ava Chen",
      "sectionId": "string",
      "sectionName": "Ava Chen",
      "type": "string",
      "webPublicationDate": "string",
      "webTitle": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `fields` | object |  |
| `fields.headline` | string |  |
| `fields.trailText` | string |  |
| `id` | string |  |
| `isHosted` | boolean |  |
| `pillarId` | string |  |
| `pillarName` | string |  |
| `sectionId` | string |  |
| `sectionName` | string |  |
| `type` | string |  |
| `webPublicationDate` | string |  |
| `webTitle` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native The Guardian API, this operation is `GET /` (base URL `https://content.guardianapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-home-editors-picks.md) for the provider-specific parameters and requirements.

