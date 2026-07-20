# Loopy Loyalty: List Campaigns



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-campaigns?${params}`, {
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
      "value": {
        "createTime": "string",
        "design": {
          "backgroundColor": "string",
          "textColor": "string"
        },
        "id": "string",
        "name": "Ava Chen",
        "status": 1,
        "updateTime": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value.createTime` | string | Campaign create timestamp. |
| `value.design.backgroundColor` | string | Campaign background color. |
| `value.design.textColor` | string | Campaign text color. |
| `value.id` | string | Campaign ID. |
| `value.name` | string | Campaign name. |
| `value.status` | number | Campaign status. |
| `value.updateTime` | string | Campaign update timestamp. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /campaigns` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

