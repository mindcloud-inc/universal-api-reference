# GraphHopper: Compute Matrix

Computes a route matrix in GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/compute-matrix
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/compute-matrix?connectionId=$CONNECTION_ID&requestBody=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestBody": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/compute-matrix?${params}`, {
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
| `requestBody` | object | yes | Matrix request JSON body matching GraphHopper's MatrixRequest or SymmetricalMatrixRequest schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "distances": [
        [
          "string"
        ]
      ],
      "info": {},
      "times": [
        [
          "string"
        ]
      ],
      "weights": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `distances` | array<array> | Distance matrix. |
| `info` | object | Response metadata. |
| `times` | array<array> | Time matrix. |
| `weights` | array<array> | Weight matrix when requested. |

## Native endpoint

Through the native GraphHopper API, this operation is `POST /matrix` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compute-matrix.md) for the provider-specific parameters and requirements.

