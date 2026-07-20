# Docusnap365: List Platforms



```
GET https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-platforms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docusnap365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-platforms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-platforms?${params}`, {
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
      "iconId": "string",
      "id": "string",
      "label": "string",
      "realm": "string",
      "resourceTypeId": "string",
      "scope": "string",
      "segment": "string",
      "userDefined": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iconId` | string |  |
| `id` | string |  |
| `label` | string |  |
| `realm` | string |  |
| `resourceTypeId` | string |  |
| `scope` | string |  |
| `segment` | string |  |
| `userDefined` | boolean |  |

## Native endpoint

Through the native Docusnap365 API, this operation is `GET /api/v2/platforms` (base URL `https://api.docusnap365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-platforms.md) for the provider-specific parameters and requirements.

