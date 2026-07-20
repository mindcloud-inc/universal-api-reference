# ClassMarker: List Available Groups Links and Exams



```
GET https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-available-groups-links-and-exams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groups[].group.assignedTests[].test.testId` | number |  |
| `groups[].group.assignedTests[].test.testName` | string |  |
| `groups[].group.groupId` | number |  |
| `groups[].group.groupName` | string |  |
| `links[].link.accessListId` | number |  |
| `links[].link.assignedTests[].test.testId` | number |  |
| `links[].link.assignedTests[].test.testName` | string |  |
| `links[].link.linkId` | number |  |
| `links[].link.linkName` | string |  |
| `links[].link.linkUrlId` | string |  |

## Native endpoint

Through the native ClassMarker API, this operation is `GET /v1.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-groups-links-and-exams.md) for the provider-specific parameters and requirements.

