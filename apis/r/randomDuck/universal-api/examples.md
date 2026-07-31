# Random Duck Universal API Examples

These examples use the MindCloud API key and Random Duck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Duck GIF by Number



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/get-duck-gif-by-number?connectionId=$CONNECTION_ID&num=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "num": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/get-duck-gif-by-number?${params}`, {
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Duck GIF by Number action reference](actions/get-duck-gif-by-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/randomDuck/latest/actions/get-duck-gif-by-number).
