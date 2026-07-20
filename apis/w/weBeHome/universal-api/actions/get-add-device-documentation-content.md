# WeBeHome: Get Add Device Documentation Content



```
GET https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-add-device-documentation-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-add-device-documentation-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-add-device-documentation-content?${params}`, {
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
      "Created": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Created` | string |  |

## Native endpoint

Through the native WeBeHome API, this operation is `POST OpenAPIservice.svc/Doc/GetAddContent` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-add-device-documentation-content.md) for the provider-specific parameters and requirements.

