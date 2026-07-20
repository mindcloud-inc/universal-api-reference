# OnePlan: Get Workplan User Levels

Retrieves workplan user levels from OnePlan.

```
GET https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-workplan-user-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-workplan-user-levels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-workplan-user-levels?${params}`, {
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
      "0": "string",
      "1": "string",
      "2": "string",
      "3": "string",
      "4": "string",
      "99": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `0` | string |  |
| `1` | string |  |
| `2` | string |  |
| `3` | string |  |
| `4` | string |  |
| `99` | string |  |

## Native endpoint

Through the native OnePlan API, this operation is `GET /workplan/user/levels` (base URL `https://my.oneplan.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workplan-user-levels.md) for the provider-specific parameters and requirements.

