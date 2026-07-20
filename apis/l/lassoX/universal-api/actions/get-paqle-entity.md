# Lasso X: Get Paqle Entity

Retrieves Paqle entity details from Lasso X by Lasso ID.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-paqle-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-paqle-entity?connectionId=$CONNECTION_ID&lasso_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lasso_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-paqle-entity?${params}`, {
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
      "currentId": 1,
      "newsHash": "string",
      "originalId": 1,
      "paqleUrl": "https://example.com",
      "published": true,
      "sections": {},
      "sectionsDk": {
        "cvrMetadata": [
          {
            "cvrId": "string"
          }
        ]
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentId` | number |  |
| `newsHash` | string |  |
| `originalId` | number |  |
| `paqleUrl` | string |  |
| `published` | boolean |  |
| `sections` | object |  |
| `sectionsDk.cvrMetadata[].cvrId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /data/paqle/:lassoId/entity` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-paqle-entity.md) for the provider-specific parameters and requirements.

