# Control D: List Native Filters

Retrieves native filters for a profile from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-native-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-native-filters?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-native-filters?${params}`, {
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
| `profileId` | string | yes | Primary key (PK) of the profile |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additional": "string",
      "description": "string",
      "name": "Ava Chen",
      "options": [
        {}
      ],
      "PK": "string",
      "sources": [
        "string"
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additional` | string |  |
| `description` | string |  |
| `name` | string |  |
| `options` | array<object> |  |
| `PK` | string |  |
| `sources` | array<string> |  |
| `status` | number |  |

## Native endpoint

Through the native Control D API, this operation is `GET /profiles/:profileId/filters` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-native-filters.md) for the provider-specific parameters and requirements.

