# Tophhie Cloud: Generate GUIDs

Generates one or more GUIDs in Tophhie Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/generate-guids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/generate-guids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/generate-guids?${params}`, {
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
| `numberOfGuids` | number | no | Number of GUIDs to return. Maximum is 500. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guid` | string | Generated GUID value. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /generate/guid` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-guids.md) for the provider-specific parameters and requirements.

