# Kiwili: Get Enterprise Details

Retrieves details for an enterprise in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-enterprise-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-enterprise-details?connectionId=$CONNECTION_ID&enterprise_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "enterprise_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-enterprise-details?${params}`, {
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
| `enterprise_id` | number | yes | The Kiwili enterprise ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Email": "ava@example.com",
      "Id": 1,
      "IsClient": true,
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Email` | string |  |
| `Id` | number |  |
| `IsClient` | boolean |  |
| `Name` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /enterprise/:enterprise_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enterprise-details.md) for the provider-specific parameters and requirements.

