# Follow Up Boss: List Unclaimed People

Retrieves unclaimed people from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-unclaimed-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-unclaimed-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-unclaimed-people?${params}`, {
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
      "metadata": {
        "collection": "string",
        "limit": 1,
        "next": {},
        "nextLink": {},
        "offset": 1,
        "total": 1
      },
      "people": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object |  |
| `metadata.collection` | string |  |
| `metadata.limit` | number |  |
| `metadata.next` | object |  |
| `metadata.nextLink` | object |  |
| `metadata.offset` | number |  |
| `metadata.total` | number |  |
| `people[]` | array<string> |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET people/unclaimed` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unclaimed-people.md) for the provider-specific parameters and requirements.

