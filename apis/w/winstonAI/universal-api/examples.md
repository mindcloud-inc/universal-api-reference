# Winston AI Universal API Examples

These examples use the MindCloud API key and Winston AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Compare Text



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/compare-text?connectionId=$CONNECTION_ID&firstText=Text%20to%20compare%20against%20the%20second%20input&secondText=Second%20text%20to%20compare" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstText": "Text to compare against the second input",
  "secondText": "Second text to compare"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/compare-text?${params}`, {
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
      "credits_remaining": 1,
      "credits_used": 1,
      "first_text": {},
      "second_text": {},
      "similarity_score": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Compare Text action reference](actions/compare-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/winstonAI/latest/actions/compare-text).
