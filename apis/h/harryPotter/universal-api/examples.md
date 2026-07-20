# Harry Potter Universal API Examples

These examples use the MindCloud API key and Harry Potter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Character By ID

Retrieves a Harry Potter character by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/get-character-by-id?connectionId=$CONNECTION_ID&id=e.g.%209e3f7ce4-b9a7-4244-b709-dae5c1f1d4a8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e.g. 9e3f7ce4-b9a7-4244-b709-dae5c1f1d4a8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/get-character-by-id?${params}`, {
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
      "actor": "string",
      "alive": true,
      "alternate_actors": [
        "string"
      ],
      "alternate_names": [
        "Ava Chen"
      ],
      "ancestry": "string",
      "dateOfBirth": "string",
      "eyeColour": "string",
      "gender": "string",
      "hairColour": "string",
      "hogwartsStaff": true,
      "hogwartsStudent": true,
      "house": "string",
      "id": "string",
      "image": "string",
      "name": "Ava Chen",
      "patronus": "string",
      "species": "string",
      "wand": {},
      "wizard": true,
      "yearOfBirth": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Character By ID action reference](actions/get-character-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/harryPotter/latest/actions/get-character-by-id).
