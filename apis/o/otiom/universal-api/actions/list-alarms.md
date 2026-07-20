# Otiom: List Alarms

Retrieves alarms from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-alarms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-alarms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-alarms?${params}`, {
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
      "activate_date": "string",
      "active": true,
      "deactivate_date": "string",
      "id": 1,
      "patient": 1,
      "patient_name": "Ava Chen",
      "profiles_accepted": [
        "string"
      ],
      "profiles_declined": [
        "string"
      ],
      "tracks": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activate_date` | string |  |
| `active` | boolean |  |
| `deactivate_date` | string |  |
| `id` | number |  |
| `patient` | number |  |
| `patient_name` | string |  |
| `profiles_accepted` | array |  |
| `profiles_declined` | array |  |
| `tracks` | array |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/alarms/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alarms.md) for the provider-specific parameters and requirements.

