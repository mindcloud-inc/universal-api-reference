# Wufoo: List Reports

Retrieves reports from Wufoo.

```
GET https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wufoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-reports?${params}`, {
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
      "dateCreated": "string",
      "dateUpdated": "string",
      "description": "string",
      "hash": "string",
      "isPublic": 1,
      "linkEntries": "https://example.com",
      "linkEntriesCount": "https://example.com",
      "linkFields": "https://example.com",
      "linkWidgets": "https://example.com",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string | When the report was created. |
| `dateUpdated` | string | When the report was last updated. |
| `description` | string | The report description. |
| `hash` | string | The Wufoo report identifier. |
| `isPublic` | number | Whether the report is public. |
| `linkEntries` | string | API link to the report entries. |
| `linkEntriesCount` | string | API link to the report entry count. |
| `linkFields` | string | API link to the report fields. |
| `linkWidgets` | string | API link to the report widgets. |
| `name` | string | The report name. |
| `url` | string | The report URL slug. |

## Native endpoint

Through the native Wufoo API, this operation is `GET /reports.json` (base URL `https://{{credentials.subdomain}}.wufoo.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

