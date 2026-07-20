# Draftable: Get Export

Retrieves a comparison export job from Draftable.

```
GET https://connect.mindcloud.co/v1/universal/draftable/latest/actions/get-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Draftable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/get-export?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/draftable/latest/actions/get-export?${params}`, {
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
| `identifier` | string | yes | The export identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comparison": "string",
      "errorMessage": "string",
      "failed": true,
      "identifier": "string",
      "includeCoverPage": true,
      "kind": "string",
      "ready": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comparison` | string |  |
| `errorMessage` | string |  |
| `failed` | boolean |  |
| `identifier` | string |  |
| `includeCoverPage` | boolean |  |
| `kind` | string |  |
| `ready` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native Draftable API, this operation is `GET /exports/{{identifier}}` (base URL `https://api.draftable.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-export.md) for the provider-specific parameters and requirements.

