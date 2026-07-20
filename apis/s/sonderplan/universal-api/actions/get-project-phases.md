# Sonderplan: Get Project Phases



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-project-phases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-project-phases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-project-phases?${params}`, {
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
      "colorBackground": "string",
      "colorText": "string",
      "end": 1,
      "id": 1,
      "name": "Ava Chen",
      "projectId": 1,
      "start": 1,
      "typeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colorBackground` | string |  |
| `colorText` | string |  |
| `end` | number |  |
| `id` | number |  |
| `name` | string |  |
| `projectId` | number |  |
| `start` | number |  |
| `typeId` | number |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /project/phase` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-phases.md) for the provider-specific parameters and requirements.

