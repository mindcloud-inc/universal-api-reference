# Hyrule Compendium: Get Entry



```
GET https://connect.mindcloud.co/v1/universal/hyruleCompendium/latest/actions/get-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyrule Compendium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyruleCompendium/latest/actions/get-entry?connectionId=$CONNECTION_ID&entry=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entry": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyruleCompendium/latest/actions/get-entry?${params}`, {
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
| `entry` | string | yes | Entry ID or name; names use underscores or URL encoding for spaces. |
| `game` | list | no | Supported game; defaults to Breath of the Wild. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "category": "string",
        "common_locations": [
          "string"
        ],
        "cooking_effect": "string",
        "description": "string",
        "dlc": true,
        "drops": [
          "string"
        ],
        "edible": true,
        "fuse_attack_power": 1,
        "hearts_recovered": 1,
        "id": 1,
        "image": "string",
        "name": "Ava Chen",
        "properties": {
          "attack": 1,
          "defense": 1,
          "effect": "string",
          "type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.category` | string |  |
| `data.common_locations` | array<string> |  |
| `data.cooking_effect` | string |  |
| `data.description` | string |  |
| `data.dlc` | boolean |  |
| `data.drops` | array<string> |  |
| `data.edible` | boolean |  |
| `data.fuse_attack_power` | number |  |
| `data.hearts_recovered` | number |  |
| `data.id` | number |  |
| `data.image` | string |  |
| `data.name` | string |  |
| `data.properties` | object |  |
| `data.properties.attack` | number |  |
| `data.properties.defense` | number |  |
| `data.properties.effect` | string |  |
| `data.properties.type` | string |  |

## Native endpoint

Through the native Hyrule Compendium API, this operation is `GET /compendium/entry/:entry` (base URL `https://api.hyrule-compendium.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entry.md) for the provider-specific parameters and requirements.

