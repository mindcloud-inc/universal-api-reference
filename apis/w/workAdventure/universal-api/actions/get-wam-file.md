# WorkAdventure: Get WAM file

Retrieves a WAM file from WorkAdventure map storage.

```
GET https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-wam-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-wam-file?connectionId=$CONNECTION_ID&wamPath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "wamPath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-wam-file?${params}`, {
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
| `wamPath` | string | yes | Path to the WAM file, including the .wam suffix. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "areas": [
        {}
      ],
      "entities": {},
      "entityCollections": [
        {}
      ],
      "lastCommandId": "string",
      "mapUrl": "https://example.com",
      "metadata": {},
      "settings": {},
      "vendor": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areas` | array<object> | Configured areas in the WAM file. |
| `entities` | object | Entity instances keyed by entity identifier. |
| `entityCollections` | array<object> | Referenced entity collection descriptors. |
| `lastCommandId` | string | Last applied command identifier. |
| `mapUrl` | string | Referenced TMJ map URL. |
| `metadata` | object | Map metadata block. |
| `settings` | object | Map settings block. |
| `vendor` | object | Vendor-specific metadata. |
| `version` | string | WAM document version. |

## Native endpoint

Through the native WorkAdventure API, this operation is `GET https://mindcloud-34294.map-storage.workadventu.re/:wamPath` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wam-file.md) for the provider-specific parameters and requirements.

