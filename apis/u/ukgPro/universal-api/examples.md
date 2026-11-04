# UKG Pro Universal API Examples

These examples use the MindCloud API key and UKG Pro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Platform Configuration Fields



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-platform-configuration-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-platform-configuration-fields?${params}`, {
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
      "className": "Ava Chen",
      "fieldRows": [
        {
          "fieldName": "Ava Chen",
          "fieldValue": "string"
        }
      ],
      "keyName": "Ava Chen",
      "keyValue": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Platform Configuration Fields action reference](actions/get-platform-configuration-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ukgPro/latest/actions/get-platform-configuration-fields).
