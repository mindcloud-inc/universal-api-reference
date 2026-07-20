# Runn: Get Holiday Group



```
GET https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-holiday-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-holiday-group?connectionId=$CONNECTION_ID&holidayGroupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "holidayGroupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-holiday-group?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `holidayGroupId` | number | yes | Runn holiday group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryCode": "string",
      "countryName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "regionName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryCode` | string | Country code. |
| `countryName` | string | Country name. |
| `id` | number | Holiday group ID. |
| `name` | string | Holiday group name. |
| `regionName` | string | Region name, if present. |

## Native endpoint

Through the native Runn API, this operation is `GET /holiday-groups/{{holidayGroupId}}` (base URL `https://api.runn.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-holiday-group.md) for the provider-specific parameters and requirements.

