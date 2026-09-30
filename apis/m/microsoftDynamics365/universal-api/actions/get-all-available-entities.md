# Microsoft Dynamics 365: Get All Available Entities



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-all-available-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-all-available-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-all-available-entities?${params}`, {
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
      "@odata": {
        "context": "string"
      },
      "kind": "string",
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
| `@odata.context` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `GET` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-available-entities.md) for the provider-specific parameters and requirements.

