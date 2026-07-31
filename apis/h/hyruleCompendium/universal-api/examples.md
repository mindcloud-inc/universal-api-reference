# Hyrule Compendium Universal API Examples

These examples use the MindCloud API key and Hyrule Compendium connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Entry



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

Example response:

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

See the full [Get Entry action reference](actions/get-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyruleCompendium/latest/actions/get-entry).
