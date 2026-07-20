# MOONTO Shopping Lists - Checkpad: Get Checkpad Details

Retrieves current checkpad details from Checkpad.

```
GET https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/get-checkpad-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOONTO Shopping Lists - Checkpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/get-checkpad-details?connectionId=$CONNECTION_ID&checkpad_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checkpad_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/get-checkpad-details?${params}`, {
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
| `checkpad_id` | string | yes | The ID of the MOONTO checkpad. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_no": "string",
      "battery_percent": 1,
      "checkpad_id": "string",
      "custom_name": "Ava Chen",
      "energy_mode": 1,
      "firmware": "string",
      "last_contact": 1,
      "model_code": "string",
      "model_name": "Ava Chen",
      "sound_volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch_no` | string |  |
| `battery_percent` | number |  |
| `checkpad_id` | string |  |
| `custom_name` | string |  |
| `energy_mode` | number |  |
| `firmware` | string |  |
| `last_contact` | number |  |
| `model_code` | string |  |
| `model_name` | string |  |
| `sound_volume` | number |  |

## Native endpoint

Through the native MOONTO Shopping Lists - Checkpad API, this operation is `GET /checkpads/{checkpad_id}` (base URL `https://api.moonto.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-checkpad-details.md) for the provider-specific parameters and requirements.

