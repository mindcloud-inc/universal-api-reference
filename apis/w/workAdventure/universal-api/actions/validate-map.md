# WorkAdventure: Validate map

Validates a map URL in WorkAdventure.

```
GET https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/validate-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/validate-map?connectionId=$CONNECTION_ID&mapUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/validate-map?${params}`, {
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
| `mapUrl` | string | yes | Publicly reachable map URL to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object | Validation findings returned when the map is invalid. |
| `ok` | boolean | Whether validation passed. |

## Native endpoint

Through the native WorkAdventure API, this operation is `GET https://mindcloud-34294.map-storage.workadventu.re/validate` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-map.md) for the provider-specific parameters and requirements.

