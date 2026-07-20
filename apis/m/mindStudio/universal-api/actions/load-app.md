# MindStudio: Load App

Retrieves app details from MindStudio.

```
GET https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/load-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/load-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/load-app?${params}`, {
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
      "apps": [
        {}
      ],
      "orgId": "string",
      "orgName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apps` | array<object> | Apps visible to the current MindStudio API key. |
| `orgId` | string | The organization ID associated with the API key. |
| `orgName` | string | The organization name associated with the API key. |

## Native endpoint

Through the native MindStudio API, this operation is `GET /apps/load` (base URL `https://api.mindstudio.ai/developer/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/load-app.md) for the provider-specific parameters and requirements.

