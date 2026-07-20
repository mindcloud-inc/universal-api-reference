# SE Ranking Project: List Projects

Retrieves projects from your SE Ranking account.

```
GET https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-projects?${params}`, {
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
      "item": {
        "checkFreq": "string",
        "depth": 1,
        "exactUrl": 1,
        "groupId": 1,
        "guestLink": "https://example.com",
        "id": 1,
        "isActive": 1,
        "keywordCount": 1,
        "matchMode": "string",
        "name": "Ava Chen",
        "subdomainMatch": 1,
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item` | object |  |
| `item.checkFreq` | string |  |
| `item.depth` | number |  |
| `item.exactUrl` | number |  |
| `item.groupId` | number |  |
| `item.guestLink` | string |  |
| `item.id` | number |  |
| `item.isActive` | number |  |
| `item.keywordCount` | number |  |
| `item.matchMode` | string |  |
| `item.name` | string |  |
| `item.subdomainMatch` | number |  |
| `item.title` | string |  |

## Native endpoint

Through the native SE Ranking Project API, this operation is `GET /sites` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

