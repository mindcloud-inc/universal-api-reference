# GatherContent: Get Structure

Retrieves a structure from GatherContent.

```
GET https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-structure?connectionId=$CONNECTION_ID&structure_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "structure_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-structure?${params}`, {
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
| `structure_uuid` | string | yes | Structure UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groups": [
        {}
      ],
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groups` | array<object> |  |
| `uuid` | string |  |

## Native endpoint

Through the native GatherContent API, this operation is `GET /structures/:structure_uuid` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-structure.md) for the provider-specific parameters and requirements.

