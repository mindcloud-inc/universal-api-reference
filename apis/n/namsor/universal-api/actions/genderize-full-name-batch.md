# Namsor: Genderize Full Name Batch

Retrieves likely genders for full names in Namsor.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/genderize-full-name-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/genderize-full-name-batch?connectionId=$CONNECTION_ID&personalNames=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personalNames": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/genderize-full-name-batch?${params}`, {
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
| `personalNames` | list<object> | yes | Array of personal name objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "personalNames": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `personalNames` | array<object> |  |

## Native endpoint

Through the native Namsor API, this operation is `POST /api2/json/genderFullBatch` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/genderize-full-name-batch.md) for the provider-specific parameters and requirements.

