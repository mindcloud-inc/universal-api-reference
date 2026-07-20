# Namsor: Genderize Full Name

Retrieves the likely gender for a full name in Namsor.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/genderize-full-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/genderize-full-name?connectionId=$CONNECTION_ID&fullName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fullName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/genderize-full-name?${params}`, {
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
| `fullName` | string | yes | Full personal name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "genderScale": 1,
      "id": "string",
      "likelyGender": "string",
      "name": "Ava Chen",
      "probabilityCalibrated": 1,
      "score": 1,
      "script": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `genderScale` | number |  |
| `id` | string |  |
| `likelyGender` | string |  |
| `name` | string |  |
| `probabilityCalibrated` | number |  |
| `score` | number |  |
| `script` | string |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/genderFull/:fullName` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/genderize-full-name.md) for the provider-specific parameters and requirements.

