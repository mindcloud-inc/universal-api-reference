# Docusnap365: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docusnap365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-organizations?${params}`, {
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
      "desc": "string",
      "gridSelected": true,
      "iconId": "string",
      "id": "string",
      "label": "string",
      "realm": "string",
      "resourceTypeId": "string",
      "scope": "string",
      "segment": "string",
      "userDefined": true,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desc` | string |  |
| `gridSelected` | boolean |  |
| `iconId` | string |  |
| `id` | string |  |
| `label` | string |  |
| `realm` | string |  |
| `resourceTypeId` | string |  |
| `scope` | string |  |
| `segment` | string |  |
| `userDefined` | boolean |  |
| `userId` | string |  |

## Native endpoint

Through the native Docusnap365 API, this operation is `GET /api/v2/organizations` (base URL `https://api.docusnap365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

