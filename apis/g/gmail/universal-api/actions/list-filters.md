# Google Mail: List Filters

Retrieves filters from Gmail settings.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-filters?${params}`, {
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
      "filter": [
        {
          "criteria": {
            "from": "string",
            "subject": "string",
            "to": "string"
          },
          "id": "string"
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
| `filter[].criteria.from` | string |  |
| `filter[].criteria.subject` | string |  |
| `filter[].criteria.to` | string |  |
| `filter[].id` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /settings/filters` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filters.md) for the provider-specific parameters and requirements.

