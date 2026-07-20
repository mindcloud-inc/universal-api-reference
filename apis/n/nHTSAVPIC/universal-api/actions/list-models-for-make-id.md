# NHTSA vPIC: List Models for Make ID

Retrieves models for a make ID from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-models-for-make-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-models-for-make-id?connectionId=$CONNECTION_ID&makeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "makeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-models-for-make-id?${params}`, {
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
| `makeId` | number | yes | Exact make ID from the vPIC dataset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "makeID": 1,
      "makeName": "Ava Chen",
      "modelID": 1,
      "modelName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `makeID` | number |  |
| `makeName` | string |  |
| `modelID` | number |  |
| `modelName` | string |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetModelsForMakeId/:makeId` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models-for-make-id.md) for the provider-specific parameters and requirements.

