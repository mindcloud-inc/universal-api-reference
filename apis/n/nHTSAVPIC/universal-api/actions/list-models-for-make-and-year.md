# NHTSA vPIC: List Models for Make and Year

Retrieves models for a make and year from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-models-for-make-and-year
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-models-for-make-and-year?connectionId=$CONNECTION_ID&make=string&modelYear=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "make": "string",
  "modelYear": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-models-for-make-and-year?${params}`, {
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
| `make` | string | yes | Make name fragment, such as honda. |
| `modelYear` | number | yes | Model year greater than 1995. |

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

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetModelsForMakeYear/make/:make/modelyear/:modelYear` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models-for-make-and-year.md) for the provider-specific parameters and requirements.

