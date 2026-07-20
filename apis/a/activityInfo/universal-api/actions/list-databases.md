# ActivityInfo: List Databases

Retrieves available databases from your ActivityInfo account.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-databases?${params}`, {
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
      "billingAccountId": 1,
      "databaseId": "string",
      "description": "string",
      "label": "string",
      "languages": [
        "string"
      ],
      "ownerId": "string",
      "publishedTemplate": true,
      "suspended": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAccountId` | number | Owning billing account ID. |
| `databaseId` | string | Globally unique database ID. |
| `description` | string | Database description. |
| `label` | string | Human-readable database name. |
| `languages` | array<string> | Configured language codes. |
| `ownerId` | string | Owner user ID. |
| `publishedTemplate` | boolean | Whether the database is published as a template. |
| `suspended` | boolean | Whether the database is suspended. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/databases` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-databases.md) for the provider-specific parameters and requirements.

