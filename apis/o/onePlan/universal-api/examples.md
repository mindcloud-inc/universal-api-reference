# OnePlan Universal API Examples

These examples use the MindCloud API key and OnePlan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Security Groups

Retrieves security groups from OnePlan.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-security-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-security-groups?${params}`, {
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
      "__app__": "string",
      "__entity_kind__": "string",
      "_ts": 1,
      "ConfigId": "string",
      "GroupName": "Ava Chen",
      "id": "string",
      "IsDefault": true,
      "License": "string",
      "PermissionSettings": {},
      "RestoreFromId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Security Groups action reference](actions/get-security-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onePlan/latest/actions/get-security-groups).
