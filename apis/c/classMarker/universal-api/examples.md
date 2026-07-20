# ClassMarker Universal API Examples

These examples use the MindCloud API key and ClassMarker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Available Groups Links and Exams



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-available-groups-links-and-exams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-available-groups-links-and-exams?${params}`, {
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
      "groups": [
        {
          "group": {
            "assignedTests": [
              {
                "test": {
                  "testId": 1,
                  "testName": "Ava Chen"
                }
              }
            ],
            "groupId": 1,
            "groupName": "Ava Chen"
          }
        }
      ],
      "links": [
        {
          "link": {
            "accessListId": 1,
            "assignedTests": [
              {
                "test": {
                  "testId": 1,
                  "testName": "https://example.com"
                }
              }
            ],
            "linkId": 1,
            "linkName": "https://example.com",
            "linkUrlId": "https://example.com"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Available Groups Links and Exams action reference](actions/list-available-groups-links-and-exams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/classMarker/latest/actions/list-available-groups-links-and-exams).

## Add Access Codes



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/add-access-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessListId": 1,
  "accessCodes[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/add-access-codes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessListId": 1,
    "accessCodes[]": ["string"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accessLists": {
        "accessList": {
          "accessListId": 1,
          "accessListName": "Ava Chen",
          "numCodesAdded": 1,
          "numCodesTotal": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Access Codes action reference](actions/add-access-codes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/classMarker/latest/actions/add-access-codes).
