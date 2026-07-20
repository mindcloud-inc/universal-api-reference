# Mural: Get Export URL

Retrieves a mural export URL from Mural.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-export-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-export-url?connectionId=$CONNECTION_ID&muralId=string&exportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "muralId": "string",
  "exportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-export-url?${params}`, {
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
| `muralId` | string | yes |  |
| `exportId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": 1,
      "expireOn": 1,
      "exportId": "string",
      "muralId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | number |  |
| `expireOn` | number |  |
| `exportId` | string |  |
| `muralId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Mural API, this operation is `GET /murals/:muralId/exports/:exportId` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-export-url.md) for the provider-specific parameters and requirements.

