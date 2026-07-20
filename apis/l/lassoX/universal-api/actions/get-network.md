# Lasso X: Get Network

Retrieves a person's professional network from Lasso X.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-network
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-network?connectionId=$CONNECTION_ID&lasso_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lasso_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-network?${params}`, {
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
| `lasso_id` | string | yes | Lasso ID, for example CVR-1-34580820. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "from": "2026-05-07T12:00:00.000Z",
          "ownership": {
            "from": 1,
            "to": 1
          },
          "relationType": "string",
          "role": "string",
          "sourceLassoId": "string",
          "sourceName": "Ava Chen",
          "targetLassoId": "string",
          "targetName": "Ava Chen",
          "to": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].from` | date |  |
| `[].ownership.from` | number |  |
| `[].ownership.to` | number |  |
| `[].relationType` | string |  |
| `[].role` | string |  |
| `[].sourceLassoId` | string | Network edge source entity identifier from the documented network graph response. |
| `[].sourceName` | string |  |
| `[].targetLassoId` | string | Network edge target entity identifier from the documented network graph response. |
| `[].targetName` | string |  |
| `[].to` | date |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /modules/network/:lassoId` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-network.md) for the provider-specific parameters and requirements.

