# LightwaveRF Power: List Structures

Retrieves structures from LightwaveRF Power.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/list-structures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/list-structures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/list-structures?${params}`, {
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
      "featureSets": [
        "string"
      ],
      "groupId": "string",
      "name": "Ava Chen",
      "order": [
        "string"
      ],
      "parentGroups": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `featureSets` | array<string> |  |
| `groupId` | string |  |
| `name` | string |  |
| `order` | array<string> |  |
| `parentGroups` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `GET /v1/structures` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-structures.md) for the provider-specific parameters and requirements.

