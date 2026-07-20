# Auphonic: List Presets

Retrieves presets from Auphonic.

```
GET https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/list-presets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auphonic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/list-presets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/list-presets?${params}`, {
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
| `presetType` | list<string> | no | Choose which preset set to return. One of: `all_presets`, `auphonic_presets`, `personal_presets`. |
| `minimalData` | boolean | no | Return only minimal preset data. |
| `uuidsOnly` | boolean | no | Return only preset UUIDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationTime": "2026-05-07T12:00:00.000Z",
      "isMultitrack": true,
      "metadata": {
        "title": "string"
      },
      "presetName": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationTime` | date |  |
| `isMultitrack` | boolean |  |
| `metadata.title` | string |  |
| `presetName` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Auphonic API, this operation is `GET /presets.json` (base URL `https://auphonic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-presets.md) for the provider-specific parameters and requirements.

