# Podscan: List Entity Appearances

Retrieves entity appearance records from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-entity-appearances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-entity-appearances?connectionId=$CONNECTION_ID&entityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-entity-appearances?${params}`, {
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
| `entityId` | string | yes | The entity ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appearances": [
        {}
      ],
      "entity": {},
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appearances` | array<object> |  |
| `entity` | object |  |
| `pagination` | object |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /entities/{entityId}/appearances` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entity-appearances.md) for the provider-specific parameters and requirements.

