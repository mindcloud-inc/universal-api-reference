# Docusnap365: List Sites



```
GET https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docusnap365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-sites?${params}`, {
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
      "buildings": [
        {}
      ],
      "desc": "string",
      "iconId": "string",
      "id": "string",
      "isOpen": true,
      "label": "string",
      "realm": "string",
      "resourceTypeId": "string",
      "search": true,
      "segment": "string",
      "show": true,
      "userDefined": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buildings` | array<object> |  |
| `desc` | string |  |
| `iconId` | string |  |
| `id` | string |  |
| `isOpen` | boolean |  |
| `label` | string |  |
| `realm` | string |  |
| `resourceTypeId` | string |  |
| `search` | boolean |  |
| `segment` | string |  |
| `show` | boolean |  |
| `userDefined` | boolean |  |

## Native endpoint

Through the native Docusnap365 API, this operation is `GET /api/v2/sites` (base URL `https://api.docusnap365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

