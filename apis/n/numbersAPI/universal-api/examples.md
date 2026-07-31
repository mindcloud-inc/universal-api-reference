# Numbers API Universal API Examples

These examples use the MindCloud API key and Numbers API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Date Fact



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/numbersAPI/latest/actions/get-date-fact?connectionId=$CONNECTION_ID&month=1&day=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "month": "1",
  "day": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/numbersAPI/latest/actions/get-date-fact?${params}`, {
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
      "date": "string",
      "found": true,
      "number": 1,
      "text": "string",
      "type": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Date Fact action reference](actions/get-date-fact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/numbersAPI/latest/actions/get-date-fact).
