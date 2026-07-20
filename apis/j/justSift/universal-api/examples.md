# JustSift Universal API Examples

These examples use the MindCloud API key and JustSift connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Person Fields



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justSift/latest/actions/list-person-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justSift/latest/actions/list-person-fields?${params}`, {
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
      "displayName": "Ava Chen",
      "filterable": true,
      "id": "string",
      "objectKey": "string",
      "searchable": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Person Fields action reference](actions/list-person-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/justSift/latest/actions/list-person-fields).
