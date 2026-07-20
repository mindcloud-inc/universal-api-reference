# Bitly: List Organizations

Retrieves organizations from your Bitly account.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-organizations?${params}`, {
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
      "organizations": [
        {
          "created": "string",
          "guid": "string",
          "isActive": true,
          "modified": "string",
          "name": "Ava Chen",
          "references": {
            "groups": "string"
          },
          "role": "string",
          "tier": "string",
          "tierDisplayName": "Ava Chen",
          "tierFamily": "string"
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
| `organizations[].created` | string |  |
| `organizations[].guid` | string |  |
| `organizations[].isActive` | boolean |  |
| `organizations[].modified` | string |  |
| `organizations[].name` | string |  |
| `organizations[].references.groups` | string |  |
| `organizations[].role` | string |  |
| `organizations[].tier` | string |  |
| `organizations[].tierDisplayName` | string |  |
| `organizations[].tierFamily` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /organizations` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

